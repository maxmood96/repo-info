## `docker:24-cli`

```console
$ docker pull docker@sha256:a337d127685abaa04a77295c711fde2c9c4ccc09de0af340965a4d715608c784
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

### `docker:24-cli` - linux; amd64

```console
$ docker pull docker@sha256:e44ef10d851e44c7942c66e9df70df36359ed1cc1f7d49a1e228b5bd525539a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57236807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e4d47cb84703dc6042823b7e29e3111074beb09b50848a31cdb9cd9565ed9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 00:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_VERSION=24.0.8
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.4
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-x86_64'; 			sha256='b506272a7f34ea056e36ba23e83593c491fd8419b0ed30ecacc42fe2eee8c964'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv6'; 			sha256='4b7ca7873d92c33603075ed9dec53a4b7573964eb09e86a3a3e4ded6f88cae1d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv7'; 			sha256='122d3220a3a7fe4d9a02fd9cbe6c342d0edc8494b4531787f3da6f85a5f85983'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-aarch64'; 			sha256='cf59a08baa32a5c8684550b836fb773e7a61a5a355a4a155d848805912244278'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-ppc64le'; 			sha256='3f16bb37487d154b2c4cff1969f7333dfc905bbd1466fcc8f10312dd3fc3f546'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-riscv64'; 			sha256='0f115f2c8a356e931524f0e182e11b0a32cd7f9af19ffecf96b59bba179d225f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-s390x'; 			sha256='ced7587be61c6c18790d4bdeab9cbace6493523ce4196417ef69d326058d3ac5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Jan 2024 00:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 00:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db5a4f146e2df1f17a2c0db7ffd672b18d1750d31c7e58e352a6536d4b7ad52`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 2.0 MB (2018457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248ec8ed73b325a9cff9ec3c5bbd2c249065ee96053dfc3beafb911ef652a195`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aed6b72066db35b8929c11c552f9e827431de2b2de62b4384a1eaed88221787`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 16.4 MB (16409719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908927dc97522b6d63aaaf9953c4095be9b24a1d080edb1ada9124d56bf41ad`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 17.2 MB (17195293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d280e8e81156b63b7306ac0701738e22b333c7a26bdd96ddafb3ec8f607d2a32`  
		Last Modified: Tue, 30 Jan 2024 22:51:16 GMT  
		Size: 18.2 MB (18202352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f6ee5ccb7fa02811eb89d903666095e18e38c42a635369912f9ba0fd11e6eb`  
		Last Modified: Tue, 30 Jan 2024 22:51:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4462dfff57f9ac45d562ae18d1ca53fef4918ae18e003d21ebf960b3ade6f94`  
		Last Modified: Tue, 30 Jan 2024 22:51:15 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a474f84a4abb535fa3a05ee5a59bff31a53d0857d4d53bab82a9f2f3684c4c7c`  
		Last Modified: Tue, 30 Jan 2024 22:51:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4a3c67fa58a943f2cf6f944f8bb56c3b816e40d0464bd5e8c3aca5de701cc6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.5 KB (393495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98434705bef4a08e840c236935559018f2e8c14b29d2f6c81f22b459547b2dba`

```dockerfile
```

-	Layers:
	-	`sha256:adf7259c076a11e87128f00d30c658f57609761ed104c85e02c839d501255d42`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 355.7 KB (355744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c49ee89b4f3977fd3e28a91c9329d98dec0a0a95049183fdcf0bf4a3d64fc3`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 37.8 KB (37751 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:7c1c18acb079d51af14b367e0ee5d4b89726440521563b8a7e958cef9a634a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53709476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5d5e78b2999e9775673dda572b6d28eef9da87500c667729400a3ca4d90652`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 00:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_VERSION=24.0.8
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.4
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-x86_64'; 			sha256='b506272a7f34ea056e36ba23e83593c491fd8419b0ed30ecacc42fe2eee8c964'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv6'; 			sha256='4b7ca7873d92c33603075ed9dec53a4b7573964eb09e86a3a3e4ded6f88cae1d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv7'; 			sha256='122d3220a3a7fe4d9a02fd9cbe6c342d0edc8494b4531787f3da6f85a5f85983'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-aarch64'; 			sha256='cf59a08baa32a5c8684550b836fb773e7a61a5a355a4a155d848805912244278'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-ppc64le'; 			sha256='3f16bb37487d154b2c4cff1969f7333dfc905bbd1466fcc8f10312dd3fc3f546'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-riscv64'; 			sha256='0f115f2c8a356e931524f0e182e11b0a32cd7f9af19ffecf96b59bba179d225f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-s390x'; 			sha256='ced7587be61c6c18790d4bdeab9cbace6493523ce4196417ef69d326058d3ac5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Jan 2024 00:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 00:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9bf8798e15e3c70ee86b4e6c377b59a1daa71177b69cf606b839f0d685b33`  
		Last Modified: Mon, 29 Jan 2024 05:00:43 GMT  
		Size: 2.1 MB (2108648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0153d86bf68c7f1f8043fdd897f7e29615f23c760458ffb36d73b68765050e03`  
		Last Modified: Mon, 29 Jan 2024 05:00:43 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06291493754ae450b19d271fdeacd19a7ad94bab7873f41c5f13cd503d43846`  
		Last Modified: Mon, 29 Jan 2024 08:03:05 GMT  
		Size: 15.1 MB (15130183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30d7ead1238714053cfa365b5f7038b942e9e97b9841d71f86e5b2357828ad9`  
		Last Modified: Mon, 29 Jan 2024 08:03:05 GMT  
		Size: 16.1 MB (16099977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9c070f6846049c4e0a28f1ba8bd39a3623b7f31ed1391d15775eabc8246d7d`  
		Last Modified: Tue, 30 Jan 2024 23:13:11 GMT  
		Size: 17.2 MB (17203010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3430b1b808592d3a43074a9315414d082fe3456c1e592824146772f95489301`  
		Last Modified: Tue, 30 Jan 2024 23:13:11 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2af6fdbb2e2ab90df9c7dd4c470a958de11d6f79efcf4bb3b05a3f927410d6`  
		Last Modified: Tue, 30 Jan 2024 23:13:10 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15012d16b2b2e1e44f023432808b4e24bac32cd0a7cc2a3c88166bc09c1ba64`  
		Last Modified: Tue, 30 Jan 2024 23:13:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6219f454f8ebdf782f524ab592c0d94f23fd36e9c9c11bf0c13c163f57faffe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3091aeb435c7d0b6b1a286bb2d678db978f8346c231c10e381c508df2b34d1a8`

```dockerfile
```

-	Layers:
	-	`sha256:9267d8902fed1655a8b47bce9d3d475d63b22627fb8868a9ea9e41e91755f68e`  
		Last Modified: Tue, 30 Jan 2024 23:13:10 GMT  
		Size: 37.5 KB (37518 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:111cb5a63173a69c339b510963a3e65d36b42cd4ae10c3e37b58531d9da01562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53195064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfbac7657b62cbc9d69124232d937e3bdee751949ad41607e70f8fc96fd9b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 00:04:16 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_VERSION=24.0.8
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcc37869d996703b2877f776d94ee24bd228d5baae5c13562b64534676ed8a9`  
		Last Modified: Sat, 27 Jan 2024 15:37:05 GMT  
		Size: 1.9 MB (1896148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ffb9edbb4cb5aef681d145a6973e8f789058991e0a84456aff999e6e85`  
		Last Modified: Sat, 27 Jan 2024 15:37:05 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb06e26c3d5c6b74794c128ba1bc95d1e5e1493d4711d2b43f18254522c5d1`  
		Last Modified: Sat, 27 Jan 2024 15:37:50 GMT  
		Size: 15.1 MB (15126554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cdc489a088357a0de2c81e3ac9c6381795927360f7e93a17349f1858efebbe`  
		Last Modified: Sat, 27 Jan 2024 15:37:50 GMT  
		Size: 16.1 MB (16084099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c1f48a032bd5f4b5dee90c6971e28f8296bfe36ead7d8c6ed9258e78c56ceb`  
		Last Modified: Sat, 27 Jan 2024 15:37:50 GMT  
		Size: 17.2 MB (17167104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63510805cbf1ee6c837c617324a2501c00d2a7541616b8730ae129e57d67121`  
		Last Modified: Sat, 27 Jan 2024 15:37:49 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0ea548e3fe337a4b99b2438333f631d5ea8b517aa72003b1f50a21172275ae`  
		Last Modified: Sat, 27 Jan 2024 15:37:50 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aad94ef3b5088410b35b18057abbb0e5e7e244ad7ab8df5dd56f5a10cc63f5`  
		Last Modified: Sat, 27 Jan 2024 15:37:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ada33705a0615b1642fc0656396051dd0715cb53b04d0c5907ac03e35b8298d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.5 KB (393513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba30fa8720df506395c23173bfde8688762f61e86846ce80982cc2121b164b1`

```dockerfile
```

-	Layers:
	-	`sha256:348bc34a95f0ee82cc387a0d4750c66dba4a8ba3966d02d1d687036b698fd22b`  
		Last Modified: Sat, 27 Jan 2024 15:37:49 GMT  
		Size: 355.8 KB (355780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf36d402c53882cbd06ec9cd1f339b9f63c63778cdc5ca7e6f4ce6218f3db90`  
		Last Modified: Sat, 27 Jan 2024 15:37:49 GMT  
		Size: 37.7 KB (37733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:73f7b7ed02462f90fa16122d364415ca13458497b79301c7e8a65620cef91364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53103450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838123b12a67d7db9ac9da0bf34fb30184c806be7a4e2032934868eda07e5d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 00:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_VERSION=24.0.8
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.4
# Tue, 30 Jan 2024 00:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-x86_64'; 			sha256='b506272a7f34ea056e36ba23e83593c491fd8419b0ed30ecacc42fe2eee8c964'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv6'; 			sha256='4b7ca7873d92c33603075ed9dec53a4b7573964eb09e86a3a3e4ded6f88cae1d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv7'; 			sha256='122d3220a3a7fe4d9a02fd9cbe6c342d0edc8494b4531787f3da6f85a5f85983'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-aarch64'; 			sha256='cf59a08baa32a5c8684550b836fb773e7a61a5a355a4a155d848805912244278'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-ppc64le'; 			sha256='3f16bb37487d154b2c4cff1969f7333dfc905bbd1466fcc8f10312dd3fc3f546'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-riscv64'; 			sha256='0f115f2c8a356e931524f0e182e11b0a32cd7f9af19ffecf96b59bba179d225f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-s390x'; 			sha256='ced7587be61c6c18790d4bdeab9cbace6493523ce4196417ef69d326058d3ac5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Jan 2024 00:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Jan 2024 00:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 00:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd627277f8af1d68caa52e5725c89976aa4c6aca5c14958e83eb2143390ab6f`  
		Last Modified: Sat, 27 Jan 2024 17:51:38 GMT  
		Size: 2.0 MB (2019693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fb61f641eda83263d0ea571074960545636883de036a62c02d9b400bf583b3`  
		Last Modified: Sat, 27 Jan 2024 17:51:37 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a7456c7e2e48e3b9172a7ee04cae83fc6b78718d7a8a4a100b97918becfa11`  
		Last Modified: Sat, 27 Jan 2024 17:52:07 GMT  
		Size: 15.5 MB (15461810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18caa195548a3e53f2628e67ea956d63cda5fde48722c22050affc79ec0df56d`  
		Last Modified: Sat, 27 Jan 2024 17:52:06 GMT  
		Size: 15.6 MB (15640600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151f5451bdb87b23c5abaadadd5829f59ebc94786efba38b5b3d68580031292`  
		Last Modified: Wed, 31 Jan 2024 02:02:48 GMT  
		Size: 16.6 MB (16631366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5a631ed90b271f319528785ca7d4f53ef6f6d6f4b337c87b3f39f8543ed308`  
		Last Modified: Wed, 31 Jan 2024 02:02:47 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70fd66672fe829e203cd2df66e66610c165deea60e2b1c0499d8837c4de35cd`  
		Last Modified: Wed, 31 Jan 2024 02:02:47 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55481dd89fc548546ad551245ad67bd9ce1bd23a820770803027a076c870d4b`  
		Last Modified: Wed, 31 Jan 2024 02:02:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0d4be38784fa89c5d846cdd4065e015139c869a96b6dfa763ec8060e1db1f84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 KB (393350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b393f9e75073a7bd495557c1336d0f7f57767805756243fa3280ef4ed38f54df`

```dockerfile
```

-	Layers:
	-	`sha256:7a74601436548491bc308e42e182cc9abb0a21981ffa7171e1a3e0e2a0237270`  
		Last Modified: Wed, 31 Jan 2024 02:02:47 GMT  
		Size: 355.8 KB (355755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61cd82a53008ffc3e0a6e23e7ea0cc246ac5caf4c5441c3ebe8d75b1d80d1329`  
		Last Modified: Wed, 31 Jan 2024 02:02:47 GMT  
		Size: 37.6 KB (37595 bytes)  
		MIME: application/vnd.in-toto+json
