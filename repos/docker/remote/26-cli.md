## `docker:26-cli`

```console
$ docker pull docker@sha256:c4452ac66ad8187c952eb88767cefbe5c72be8f814a7308f8ca5b0ba46f29252
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
$ docker pull docker@sha256:427812fc5acb577e97557076496f655bd0768cfd5b2e6f038bbcfe13e0d9b866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60303080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88607e5c76f51d60858f711dee462bc878cc788624c707f95fc61ae741da00b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Apr 2024 23:17:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_VERSION=26.1.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Apr 2024 23:17:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 23:17:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612d43df1825367f3e7cc460359712d50edb80d67eca85b14fc4baaef3f3cc3`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 2.0 MB (2026160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7104dac865754166d18a32ae6d1ced2a3bc9dc1ec76f1de5a54dafbd2e3de39`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65d5c017567733fcb8fdf52038260d2884ff55eeb6ac010dd36e4f32359dcb6`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 18.0 MB (18023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ef7f86d9f84e411c695f63a8b8ec14f5b0aa348865fa77adc404a156e0f588`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 18.1 MB (18078214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7cca4f6a3581c5f911f9bc9837add1296f07c6cec3707a7ccac031323d32c`  
		Last Modified: Thu, 25 Apr 2024 18:52:13 GMT  
		Size: 18.8 MB (18764669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd619a5b8413dfe87c9aafc5a7adc67aa3e18d4d447732ebae72f71859f9c9cc`  
		Last Modified: Thu, 25 Apr 2024 18:52:13 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556c27015097c8fd89beda2486392ddf5c0db1c48c81a203bba6ef3893d677c4`  
		Last Modified: Thu, 25 Apr 2024 18:52:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedc2ef270f1a9ac503de7af81b62da42bee0dcf5ddfd8ef7845e4e43585b2`  
		Last Modified: Thu, 25 Apr 2024 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a5af29d6788871eb41222c76a2d2d487e6f3f37b0a5231a30de83d0c7644dc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.1 KB (428062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb012818eb5f6bec46e1645250b75c0edfcc65d814f7c8d46362803a0b14a58`

```dockerfile
```

-	Layers:
	-	`sha256:a813361ded36df73914ff91c35456926d09405751ee80a8b42e1dcad294a5b81`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 390.0 KB (390015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a551b9a64958a56e92d7d138bbb2e106dc7ebcb11767f997c9ea407dc2b2904d`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 38.0 KB (38047 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:156ded96dbcf174b5522d5a5d97f786d57d0884b98fda7f16474f64eab580406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56243705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb7f1af61ef686e7e7d3ad25c69deaa3255e29a03520a64618d7a0b0859e05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 24 Apr 2024 23:17:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_VERSION=26.1.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Apr 2024 23:17:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 23:17:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df81b92ba1f4156d8bc09cde32c3c3acb72b2f836feed84f459a8fea520b95f9`  
		Last Modified: Thu, 25 Apr 2024 18:55:41 GMT  
		Size: 2.1 MB (2116804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcda65bc8fc7021d053af60b2ed4275e6fb0af9165da9aad60f3294b016a4d2`  
		Last Modified: Thu, 25 Apr 2024 18:55:41 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bd24dfe95650bc354d06643eb02e6d779571adcdf54ff7fe96f3ff0262fba3`  
		Last Modified: Thu, 25 Apr 2024 18:55:42 GMT  
		Size: 16.3 MB (16316781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c932ef28687bcc82b56ea1b136711536afe74073bd93bbeba9c3567d577d15a4`  
		Last Modified: Thu, 25 Apr 2024 18:55:42 GMT  
		Size: 16.9 MB (16915891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8979c2c753423e4a40d511b21c9a535c4ca6b91e39c8d47f2b65271029be1`  
		Last Modified: Thu, 25 Apr 2024 18:55:43 GMT  
		Size: 17.7 MB (17726572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc07250aa40bb6a3a5370a9321803e53cdd78849ed024d08b4d17ac2e479feb`  
		Last Modified: Thu, 25 Apr 2024 18:55:43 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de602837a1d71055545866ad31ae41bed499aeb9ce2453a2ab915f74de22ef59`  
		Last Modified: Thu, 25 Apr 2024 18:55:43 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5720df65ec9f5dad918a43e510e9775ab71e2d27e0a24670296d053b66f11`  
		Last Modified: Thu, 25 Apr 2024 18:55:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:85392ee628eec0455889d9c83fa7d74df7026d14bec5f85c1876c3bdbe2beac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a686a50b3e16a2e4866d037b1b029e93f92f9fd0183e9f48c6cb9f933313fb0`

```dockerfile
```

-	Layers:
	-	`sha256:a88e55ece9fa7eb3bd8dd7a56ae4d33b5d9d0b412ff5d11d3ad26736e3712b77`  
		Last Modified: Thu, 25 Apr 2024 18:55:41 GMT  
		Size: 38.0 KB (37984 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:46edb930a45f93055bd3c12f6c0d18d863a28eb19d3b16fe8ac5d70dc2593c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55739172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454fdfa70197c162f91861b5781fd75bb46de16c964755d9fbdcbd79d1f60862`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 24 Apr 2024 23:17:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_VERSION=26.1.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Apr 2024 23:17:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 23:17:38 GMT
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
	-	`sha256:5efd175250621532632e98c4b812471d1016341f3f5fd5a069bbad4d7a268ee5`  
		Last Modified: Thu, 25 Apr 2024 19:05:15 GMT  
		Size: 17.7 MB (17710688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065c7c6c39542590fb238bd5e5b65ef71428c277536c22ff77747059e95ca511`  
		Last Modified: Thu, 25 Apr 2024 19:05:14 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9595d85cdf1718473c35a3caf8c8a862b0c599076b193b9860182b3eb66c9e61`  
		Last Modified: Thu, 25 Apr 2024 19:05:14 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6708b32f17b3dab048216769e865060dde6131fee29335f04dbd0d0d93c5b00`  
		Last Modified: Thu, 25 Apr 2024 19:05:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:71d78bf5bf44215203c4f4a9476b7450fae5eddcfab3c448ae6e231cd3c56368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 KB (422627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e16de62c30800e0b24991f009a08f1a03c5bb591a3de1c4519825c61c3d647`

```dockerfile
```

-	Layers:
	-	`sha256:98f2cd336d425ecaf5a97778819ab8472ed36f7fa92d64404932933410e9eba9`  
		Last Modified: Thu, 25 Apr 2024 19:05:14 GMT  
		Size: 384.6 KB (384590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0d798e80bc295b0ab1b3b81903491c027e537e01c81588ef3a7da35134d43c`  
		Last Modified: Thu, 25 Apr 2024 19:05:14 GMT  
		Size: 38.0 KB (38037 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ef6099d3537a6a5602d6934a8932767d9fc4e485ae4a3f5df9cf1ee7ec812374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55925356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f42764f0caee1e800c725831d78ce581bab0ad1583640bd9e8cb95dec462181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 24 Apr 2024 23:17:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_VERSION=26.1.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 24 Apr 2024 23:17:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Apr 2024 23:17:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Apr 2024 23:17:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 23:17:38 GMT
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
	-	`sha256:45893ede12b2a8cd3cafbf11fc1e909680568b3bf4aa0e12671746e1d02eb7b5`  
		Last Modified: Fri, 26 Apr 2024 07:42:42 GMT  
		Size: 17.1 MB (17134334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c160af08b1a4c00c222ececab3ec6bb1aee7c4b94bd61de1ed3fa48542d0d37b`  
		Last Modified: Fri, 26 Apr 2024 07:42:41 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae43ff3ad9798028b24ad2c990cee8712709c7d0c59bf84614ab5692e4fa5325`  
		Last Modified: Fri, 26 Apr 2024 07:42:41 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e263e8ec0a0e5e87744a80b7e8b8cc0ac653f780f6789d30742c7f3a32b178`  
		Last Modified: Fri, 26 Apr 2024 07:42:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:15611d3ba452c058bdd3d098fdaf0f8897ecf14aacc84e08bdcf56205008f2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.0 KB (422952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f0ced2cdad7499589fe7373de188eb590bcd1d90e3dd71881c7f80d0dc68f`

```dockerfile
```

-	Layers:
	-	`sha256:9b1d3ac27a5ad1d0674bf52beb4836f2a6cf5e71c6aac86031a4e5d62c241e28`  
		Last Modified: Fri, 26 Apr 2024 07:42:41 GMT  
		Size: 385.1 KB (385059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881e0fd92da3ed700c71eb20e51b332aa6605af0f8fdde44df590d3e5422ce8d`  
		Last Modified: Fri, 26 Apr 2024 07:42:41 GMT  
		Size: 37.9 KB (37893 bytes)  
		MIME: application/vnd.in-toto+json
