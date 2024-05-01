## `docker:cli`

```console
$ docker pull docker@sha256:6f9767890938d2b6cd39b4dcc67ed8747b119dd3f766c8600a99fcfba80a9133
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
$ docker pull docker@sha256:6d2c943ad36653f0f7809a5200e1303f4145098c7c326e751b34a69eabd27540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60303200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1519cbc22b0c151ccd47fdfa5610f0b07cd1e0a9826c26c960b177ac9514be20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_VERSION=26.1.1
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f1d5d472fe15223da6e43b59ce342f0e98d80664562b2a2b14259f23862f5b`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 2.0 MB (2026154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd324c58b14eee17de7e63a209be9a6b28cc90f05ef54a2abfee462a2051012`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560af3c6f801629d1eab1b09a057f80c8a9516cd70ebfbfecaa0bea2a3f8f62e`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 18.0 MB (18023175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d56477ff9db9738ad3a1e4028529cb140cc263449b4da5dd347eb519c8c3ae`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 18.1 MB (18078213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e17c23668a49531c2bd081e90967fef76f57d1d981b5bdb4c28aaefd19e4d4`  
		Last Modified: Tue, 30 Apr 2024 21:49:49 GMT  
		Size: 18.8 MB (18764669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef3cdaccec305bb0cf40ecbdc31d2f48f6ebb223beb6fad36272cbd1904f60b`  
		Last Modified: Tue, 30 Apr 2024 21:49:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c82127e9726872164eeb8dd0adfa8042361456cb1ca0fc559bdb592abfd60d0`  
		Last Modified: Tue, 30 Apr 2024 21:49:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a53779d90e189c1ef9fb0d61a8417cabb02131a963fe7608e99676bdeab4160`  
		Last Modified: Tue, 30 Apr 2024 21:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:70006bf5dbc0679abb47918dbf0a3ebbf9def688f1d115b108e8bc2590f33663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.1 KB (428062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2029fcadf60e1ab99ea207170a6b4fed4c935fc323fc06e5327dc28b4265935e`

```dockerfile
```

-	Layers:
	-	`sha256:f31eae836b5edbbf31b3fb48da4eb93971713090edaeb9a8cca371cbd21003dc`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 390.0 KB (390015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6333b2dc6bafde99a31a6e6aa2d7ec69348082c3956b9a54bbf2d9c2478fa7f6`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 38.0 KB (38047 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:46dd096a67ceacf88cf5604d2edbe2f0c6088f81fdabe9a84f74300222f8e2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56243613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715d7e210f325a8c83a2d9a7f6a973e069401b907695f829b7e9629d7ddafd68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_VERSION=26.1.1
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0b230aad35f2b78ce4e1ec560de2a832387672d5c9b4315323ea10891ba2a5`  
		Last Modified: Tue, 30 Apr 2024 21:53:20 GMT  
		Size: 2.1 MB (2116779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574d227c87acd211ab67ad21e6eccc838099ecd4a9bc05e5b7a30342bf114f0`  
		Last Modified: Tue, 30 Apr 2024 21:53:19 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f52789929cb96ca51f82d607016d836f188edd2bc60fac7635a76b425c4604`  
		Last Modified: Tue, 30 Apr 2024 21:53:20 GMT  
		Size: 16.3 MB (16316721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230ce9b3c872cfdf2a05f8742977c1653e259294ebd3de9058e35254077b24b9`  
		Last Modified: Tue, 30 Apr 2024 21:53:20 GMT  
		Size: 16.9 MB (16915879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46936893ef39e45bd39ff16095c9fd6f1916ea0216e469a21b944c1f1fa589dd`  
		Last Modified: Tue, 30 Apr 2024 21:53:21 GMT  
		Size: 17.7 MB (17726576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cab2e4ad789d0afef8aa63050e5446a8dbc9f722b86e307c5357ab58772e1f`  
		Last Modified: Tue, 30 Apr 2024 21:53:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc07b9b264c1e8db63eaeda431ed3508bda55e4ff4735a0a4a4e0962ff3ad499`  
		Last Modified: Tue, 30 Apr 2024 21:53:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b83fab74de503313dd1ba1d8a6f8702ffe5ea2cf8e0c97f41a90ca17f51e32`  
		Last Modified: Tue, 30 Apr 2024 21:53:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:124308c1d0466bb4ff1e8b6414ebcd06cdede1098105f56bce57ccbe89ba6e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d67501cce6b928f326362f7884bc3bbd443626c7acd2a8c5e529f09774d11d`

```dockerfile
```

-	Layers:
	-	`sha256:d06e750b8b740dbe46974b3409db480809fbcd71b404c40b9131b526d061a34c`  
		Last Modified: Tue, 30 Apr 2024 21:53:19 GMT  
		Size: 37.8 KB (37818 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:d059c35977c1c53797ccd076679283891d63c8ba10982b06f2450e1eba14da19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55738878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cc7e125d4b37c2949ca9d3f7c55cbf882106965673a7dfa289afc04364e019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_VERSION=26.1.1
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
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
	-	`sha256:31e2653da14679cfb0a8eddcb755883e0a705fe3e5b98db684ca67214185b368`  
		Last Modified: Tue, 30 Apr 2024 21:55:44 GMT  
		Size: 16.3 MB (16308957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd1168a48c947a0af62ec3ff5c1125165b2dcb86aae2f5e3884c668716c7b72`  
		Last Modified: Tue, 30 Apr 2024 21:55:44 GMT  
		Size: 16.9 MB (16901914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c74aeaf0ec4420a40bd73fcb89ed96386fd33f0d3daf0c137ff72397b62424`  
		Last Modified: Tue, 30 Apr 2024 21:55:44 GMT  
		Size: 17.7 MB (17710686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc77c003f0ee7e0981cb46480e88838b6d827004e54ce53d5490ac5589b6b7`  
		Last Modified: Tue, 30 Apr 2024 21:55:43 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a8dd3735136a6bcc4749d4ceb777f060e485f5f8f2e71f3d9c81873b4a0f3d`  
		Last Modified: Tue, 30 Apr 2024 21:55:44 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd7c434e06f9070e3827409cb1d1110455a65a3bad56fd12bb7a425559012c3`  
		Last Modified: Tue, 30 Apr 2024 21:55:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0ff27ed9ef3d1949edbcfb1cb7eb11db69ac401b214363047deb65ab5ffbe6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 KB (422626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b12c2ed9c78847c2b3fb6297978c4159a3f8d968e392308b14c55f5d3152342`

```dockerfile
```

-	Layers:
	-	`sha256:e0177e252994181639fff8ac0adea61579ce109e31cbdb5397a78aa90e4078ab`  
		Last Modified: Tue, 30 Apr 2024 21:55:43 GMT  
		Size: 384.6 KB (384590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a2b52b528111250635c86052c2940ca2b820bae2e24cd4ace4943a6a62eb8b`  
		Last Modified: Tue, 30 Apr 2024 21:55:43 GMT  
		Size: 38.0 KB (38036 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

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

### `docker:cli` - unknown; unknown

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
