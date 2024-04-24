## `docker:26-cli`

```console
$ docker pull docker@sha256:eeee95a830f73093b89dd99d1c37d159694528a5683adae6e8e39fe898af41e7
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
$ docker pull docker@sha256:2be2afe662c8e41b7a1a5d0320169ae96e5c074619a3b9ce9f11ee20571bdb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60207920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31f849501a7441412e55fc91080a93f5bd1861c36041968a3c08f911f996501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_VERSION=26.1.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Apr 2024 21:49:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3147f52f6f5e9e3a9d762a348e40010ff2071a23acee00bbc447f0508319d5`  
		Last Modified: Tue, 23 Apr 2024 23:52:16 GMT  
		Size: 2.0 MB (2026157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259973fcd3f1e6876208a8705b2e3c566c2e17c71f2f310a81087ee84e138e68`  
		Last Modified: Tue, 23 Apr 2024 23:52:16 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ad4503ad4ed332cbe5ebd1a8e31b4e69dd60ec02bee74a7d1f7632833b396`  
		Last Modified: Tue, 23 Apr 2024 23:52:16 GMT  
		Size: 18.0 MB (18023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7ebff1d1ead17a1b89cfab4c73a7af1c823237466c5b5291d300efea446f48`  
		Last Modified: Tue, 23 Apr 2024 23:52:16 GMT  
		Size: 18.1 MB (18078217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d942f6bebc7940a6464e254e882d4c2d91e83d34fab8914f40026895b9c3fd7`  
		Last Modified: Tue, 23 Apr 2024 23:52:17 GMT  
		Size: 18.7 MB (18669509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a90a41d7f22de24aa5b5307c7a6b36b400fe7a7db8585a4dee963f2ef626d46`  
		Last Modified: Tue, 23 Apr 2024 23:52:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b68e40426b131a5babc7bc5b1e6fe4c0e0ae819c7d8d3263dcfaed916e5dd5d`  
		Last Modified: Tue, 23 Apr 2024 23:52:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ad06dcbadc52b4a065b3a7ce31d043b3a582e0e9a3d0f400daf4f2d36a9ede`  
		Last Modified: Tue, 23 Apr 2024 23:52:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6018a7fb8a991ce4ee2724b4d703c45e09ac6a20caf5036eb5ca832b11ed3f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.5 KB (429525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4455ebc61f92dbad741d347ce3b4a12524619424724a8559f0fa7cbfb669e5f`

```dockerfile
```

-	Layers:
	-	`sha256:3a8454a83d8fdbfe3e837422443a90b4c70af62ff04a8ec5bf4aab642c1f5420`  
		Last Modified: Tue, 23 Apr 2024 23:52:15 GMT  
		Size: 391.5 KB (391478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee8ea930b56a66591746893755985e98d26b633d814b9be51293a59454693e2`  
		Last Modified: Tue, 23 Apr 2024 23:52:15 GMT  
		Size: 38.0 KB (38047 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:5d8608e31f2aecadd42d376750132d95e62d4de7de6b5e01d3f1aa1f7d3073ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56148590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabb3c2a927aede7acaaeb24de626afa0c00b365e8c20591e1fbf645fdd46c55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_VERSION=26.1.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Apr 2024 21:49:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0367a9016d30be090df4c0b098c7a2d8efb3ad2b210d986c46c27ac0cdfa70b`  
		Last Modified: Tue, 23 Apr 2024 23:58:50 GMT  
		Size: 2.1 MB (2116801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3299d0af94957bf26b3b6210958926aa008849af7f7e5f7f6b373f1387b440a6`  
		Last Modified: Tue, 23 Apr 2024 23:58:49 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed31868465424e4f1d87c900e969e03abd338bf535cfc3492aad1b6620730c6`  
		Last Modified: Tue, 23 Apr 2024 23:58:50 GMT  
		Size: 16.3 MB (16316780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8132f3170bc3e4b9530cc827edd84f744982a98c71869e89cd58b83a7ebcda8`  
		Last Modified: Tue, 23 Apr 2024 23:58:50 GMT  
		Size: 16.9 MB (16915877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5affe2c7919675ce59165d3cf2ef4f8a87cf564b347e88c0682d68cf37cf105e`  
		Last Modified: Tue, 23 Apr 2024 23:58:51 GMT  
		Size: 17.6 MB (17631473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33d379a177c58d507cddc9806f577ab66855887d8b705ba561fa8b1ebb6685`  
		Last Modified: Tue, 23 Apr 2024 23:58:50 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35c8aba25e5f7947aec8eb2b6572c855fe42269a043daba26b47e6920d30e3b`  
		Last Modified: Tue, 23 Apr 2024 23:58:51 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e20d35f8c8b31ef50082b616df37c8910b7760b32b969227db16bd78bbb444f`  
		Last Modified: Tue, 23 Apr 2024 23:58:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:24f5271ffa4fb20a8ada774c475b7135cf3f92734856aeabde1ac8f29c30b3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e7ac67170b6f5d67fb47c914f578dd785e8aa1f11f62b17cbc1b7f9d777750`

```dockerfile
```

-	Layers:
	-	`sha256:42b09e6f988cc230b073f8ead317fc9966c6bef7712899aaf9492eebccf70ec2`  
		Last Modified: Tue, 23 Apr 2024 23:58:49 GMT  
		Size: 37.8 KB (37817 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f36f70a4ee65fd73228409bbf1bca651395eab88eb86c42e121e761c7695bdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55645083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a46d4bfed4aa763a2ec64a631a8d2751e0474250b475b6db8501e36bee4dd1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_VERSION=26.1.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Apr 2024 21:49:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
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
	-	`sha256:5b997f4a09b13721711ce7c71b8f509e7b0019d149ff8cc16ffddf8e42df2f17`  
		Last Modified: Wed, 24 Apr 2024 00:23:28 GMT  
		Size: 16.3 MB (16309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a27cacf881615cf414b1487293c399bd22894746376e675dd833046a298851`  
		Last Modified: Wed, 24 Apr 2024 00:23:28 GMT  
		Size: 16.9 MB (16901909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdc91045bbdfd93bca73e164def207f489d4114cff16fbc626f1f1cbe08c2d7`  
		Last Modified: Wed, 24 Apr 2024 00:23:28 GMT  
		Size: 17.6 MB (17616612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdda4b5e1b5b57f2e36f8e2fa84d479d379b11e63e30378d1def794f458e03b`  
		Last Modified: Wed, 24 Apr 2024 00:23:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515671191e0fd05fd4eb343971efda0c609f631e2bc8ba1d299e68db2a6a244`  
		Last Modified: Wed, 24 Apr 2024 00:23:29 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab189f9c8f04d84052c1229b4ded096f115e969d686790e697eb51e06ae3f36`  
		Last Modified: Wed, 24 Apr 2024 00:23:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:63c6dbbf12b53041ea188667c817d7e6000d69271c321f316b375a3e90d659d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.5 KB (424481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2181fd0055ca64150805e7771e8f4db2afd44c819a8b094d3288fa45434d3`

```dockerfile
```

-	Layers:
	-	`sha256:e5d2b8f365c84d15b56f82601898b3a1bdddf9b5a67b44fe34384d09c28d8d06`  
		Last Modified: Wed, 24 Apr 2024 00:23:27 GMT  
		Size: 386.4 KB (386445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d2f49fa204af45123bdb7e5f2c2de6b82fcbc6223c68d26a8ce790925c7d373`  
		Last Modified: Wed, 24 Apr 2024 00:23:28 GMT  
		Size: 38.0 KB (38036 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:135b4369d491f2d702b958719d38c30460ee70b3d9f5e6f436f42f52449b8382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55838153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec768daf5e5152fa9c12df018602e67c7ad0ce1761a4bcc08f2cac0d11116a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_VERSION=26.1.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Apr 2024 21:49:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
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
	-	`sha256:d6cb7f8dcca06497c57484ff8eb9a5fa47eff1d2b450ea5e313808885d75d49f`  
		Last Modified: Wed, 24 Apr 2024 01:34:07 GMT  
		Size: 17.0 MB (16979682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0074d7eb4eefb10d90fef4e52563f5003cc933e5eaeb53fe23c881daa9e021`  
		Last Modified: Wed, 24 Apr 2024 01:34:07 GMT  
		Size: 16.4 MB (16441655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9c6299c0882bcc84d03062288bf0cd7fb74a4b3dd4f1d6ff6ecd354966da1f`  
		Last Modified: Wed, 24 Apr 2024 01:34:08 GMT  
		Size: 17.0 MB (17047136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb177eab0b0431234b61ab934a94791cbecbd5b6e44591ede4c466946d0e737`  
		Last Modified: Wed, 24 Apr 2024 01:34:07 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22085cf3c8676c6a0eba65f96551c7f35e9b9149a85f6b07b4a1ccc99e6b271`  
		Last Modified: Wed, 24 Apr 2024 01:34:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f10a6ec2c2b7aa8439911a911d901949a6d1a94c18e2aaed2ea91c3543eb23e`  
		Last Modified: Wed, 24 Apr 2024 01:34:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e3a26ffc9e8b30b75683e4012d5c434fe85d90cfab9860e9c45ec81c62889b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 KB (424415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f747ba5652695ce46c9070161405b01050df3806fcd78355cc41c9477d9e5d`

```dockerfile
```

-	Layers:
	-	`sha256:9483ab12353c1d302e224905118fdd609dd25c072dad9379814c96afd1aadb02`  
		Last Modified: Wed, 24 Apr 2024 01:34:07 GMT  
		Size: 386.5 KB (386522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf39c1e51cc49efcfd5ac1b005afe34633e071f3ec516054d4873e92f0e241b8`  
		Last Modified: Wed, 24 Apr 2024 01:34:07 GMT  
		Size: 37.9 KB (37893 bytes)  
		MIME: application/vnd.in-toto+json
