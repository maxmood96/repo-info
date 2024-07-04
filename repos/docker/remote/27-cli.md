## `docker:27-cli`

```console
$ docker pull docker@sha256:a859d321553b55163a029a5a8736c229d99d28424f4e1c628e2128f57e672863
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
$ docker pull docker@sha256:ca92f169b5ea2781274ec964febb6086a52c77de4911a79d50f5a6d45f3982bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66537488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3ea62f019742f8d22ee7b14ebc79d0a5d613b498de0f60dd1fe61d6195ca3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 21:37:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea18b09b0fcf30f41de316e4be4630fa0085dd94362b76aaae0c35827240fe63`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 7.9 MB (7870364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c587ddc277589bb9c72eeb5fbbcf6860bd0465893f589c4c3e0a4b6134f170f9`  
		Last Modified: Wed, 03 Jul 2024 18:59:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725fb2fbdc90fe93a63ef892f3d1b10bbed51d4791123b7f52765d01026bfff`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 18.1 MB (18069816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd7f4f004af27720761919213789283fca9b94ec840fac6dc63771b863dc209`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 18.2 MB (18178863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f2aba2b6c7d97d70869735f836b2fbbd83375594cef8bdb99340d4fcc1368`  
		Last Modified: Wed, 03 Jul 2024 18:59:09 GMT  
		Size: 18.8 MB (18792449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e3db14824ad6370d69d2b0a3734a1320fbc7748d59560e01317cd4fc7f9898`  
		Last Modified: Wed, 03 Jul 2024 18:59:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f815063ff6c589428018dd82119692cad98408cccf8120ba6a901c9af6947308`  
		Last Modified: Wed, 03 Jul 2024 18:59:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad1a5a3e7f7e049ed56c2463db4a985f16cf9b868247be666062a9bce642601`  
		Last Modified: Wed, 03 Jul 2024 18:59:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:32941583606d9eef9b00e09342589b49047efb2434f0819d326cd0b3a0a02ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa16fa0552f980be8762f1fedf0916194a2b4aef9fe8435ed1dcd534d81112`

```dockerfile
```

-	Layers:
	-	`sha256:b71ca9167b301bdc74cbd841a22df0b71b71bf10b42d079e441313ae4b1d41d7`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:97381d85574c0131f47299c3ddcfadb43eb9013b45ab91ede3eb99d6fcfe2de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62278562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2d14a79fc53c733867fba691f21e94f1184abb0a0e33a871fd507f23bc6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 21:37:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfeb2003b64a3510951cdee1b23367446ef14e267b9b7ca4781a09809f69215`  
		Last Modified: Wed, 03 Jul 2024 18:59:06 GMT  
		Size: 7.8 MB (7801046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a05758aa32aec5f4e80ec82e4afc5cb6b200a6f65ff4aebaa5a75f6907a20`  
		Last Modified: Wed, 03 Jul 2024 18:59:05 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f3afc9302b4993803b1b0f592eaa8758c46f6f8457274a5fb7d6ca800f2526`  
		Last Modified: Wed, 03 Jul 2024 18:59:06 GMT  
		Size: 16.3 MB (16345552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c44e401e67e43cfca9dd5ef13617faea2d182c090dc047848df380b742476b5`  
		Last Modified: Wed, 03 Jul 2024 18:59:06 GMT  
		Size: 17.0 MB (17010829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32940c50a2a1686a1283a8e89b2542d0e11f641abb2fec974d485a67e361a773`  
		Last Modified: Wed, 03 Jul 2024 18:59:07 GMT  
		Size: 17.8 MB (17751827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3c852aa7ad688303a6cf8934c4dc02c778b82832f7531607fae534e1ee2da9`  
		Last Modified: Wed, 03 Jul 2024 18:59:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371fcd5c00ebd6ad222e0aa4ec88a71fe4fce3c8d8126cdf82a7c3d72c721c98`  
		Last Modified: Wed, 03 Jul 2024 18:59:07 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648c440ef60ffeb9b920da024079144062e96f5f7826d6570e04dd07bc067b50`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:877ec2b7014e3f0e8d41cabe961acef1bc945c7acfeb6ae8894f7df08c39ce84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363dd6dc3975eca6cc31a98509ec3a93cd07443a8711ddf549b2890c60f09355`

```dockerfile
```

-	Layers:
	-	`sha256:6600c75e3d5e84444125099edb161a29282abedf2a43af7f48f516cee3727a12`  
		Last Modified: Wed, 03 Jul 2024 18:59:05 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1f3722aaed080797d9d9065bb68c3b24ce5df866f2c69d19181926787bc96f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61311349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a1a1b97f8258683a741881accf6250371df88e7ee9f5fc672dd5ce9f941072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 21:37:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b684400d12517e9572d17fa04c13284bc751f64e7c32733b1e31613d957319`  
		Last Modified: Wed, 03 Jul 2024 19:58:11 GMT  
		Size: 7.1 MB (7140901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9a281c7cb0cf11879cec30177bc3e4c694f9728dc15358742f7c4bc62b128`  
		Last Modified: Wed, 03 Jul 2024 19:58:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0a299470b8fe53c9e6f5d12fe2f7388faaa8add55a43bedfb84e5538a641f`  
		Last Modified: Wed, 03 Jul 2024 19:58:11 GMT  
		Size: 16.3 MB (16339187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f75d8a56741b55aefd4b8be2904024e8896c2cdbf4cbb92651ad0f37717b71`  
		Last Modified: Wed, 03 Jul 2024 19:58:11 GMT  
		Size: 17.0 MB (16998013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f14e579dd8a6f22e6f25aecb26b4965dc6a1c1cf3f5e1b36b42cea86c42b8f`  
		Last Modified: Wed, 03 Jul 2024 19:58:12 GMT  
		Size: 17.7 MB (17736237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a29ae89beda794c7dcf19b6f51cf8018ef44db3dc204903dfe636e63e9f7e`  
		Last Modified: Wed, 03 Jul 2024 19:58:12 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef639d66c3279c578c5f2d87e80893792bbb8523fe5cddc6ee2a091b666a15b`  
		Last Modified: Wed, 03 Jul 2024 19:58:12 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ef5239f2509905e394927770ccd4e119a7c38abe5d76d82ba5956e7d3c065f`  
		Last Modified: Wed, 03 Jul 2024 19:58:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a4002340501a15c5400aaf56ba85f247155e2cdc62cd39053dd77373048c2845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b658f3663c79ebb60fff58e1abd4ae32dddb93902d9ea3debf159edb13d60c10`

```dockerfile
```

-	Layers:
	-	`sha256:c0d72cac942f1796ca4e8607058a10f02c0383720b2e573d6707c3c16fb713c9`  
		Last Modified: Wed, 03 Jul 2024 19:58:10 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b4545936d0e11b070559d08a3f6b52adb3dac0862f4daac2290e7f1de99f3af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62786426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f097a85e59dc868356613a172a082857dea3a7659e91bcbe7305e747d01b8544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 21:37:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d0a0e3728c638822326d4bd5741e292d7e5ff128e1ca81be05bf3dd691c8ed`  
		Last Modified: Wed, 03 Jul 2024 19:22:52 GMT  
		Size: 8.0 MB (7976917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4644cf50cadd0e57adc9327b67f3ff25a810337384ce8eda69b6fd36e3b76e`  
		Last Modified: Wed, 03 Jul 2024 19:22:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8d8c1a1efde10d9dcf86ff6c7668c5cf4a06e301df832937824f473c0277b1`  
		Last Modified: Wed, 03 Jul 2024 19:22:52 GMT  
		Size: 17.0 MB (17028613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab207bffba8887154ad82826c5f66b1c63c186b75561b1d7bd160dd97eb57cdf`  
		Last Modified: Wed, 03 Jul 2024 19:22:52 GMT  
		Size: 16.5 MB (16538043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e63d18d586c1d5c41def684ba0b50f47483aa044eb408710beea6b177bcbbd5`  
		Last Modified: Wed, 03 Jul 2024 19:22:53 GMT  
		Size: 17.2 MB (17151904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d71d5104b3b8710c683e69f394d30820ef8eee4fb63895116e3c3569cc6245`  
		Last Modified: Wed, 03 Jul 2024 19:22:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debf694d3effa8c3910673e0202a28f9bd04ce22846c12863c3026ad9999352e`  
		Last Modified: Wed, 03 Jul 2024 19:22:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5ce67d342e7c6ef4606557c466c2e83b5cc9f08d6cdf9c6ee86f6fb51b2d22`  
		Last Modified: Wed, 03 Jul 2024 19:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4cdbec21735d010f0464c022cadca931640f6a2a00bf3e4c686e87c9d2c66cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c01b32e9d4f3a444e8c84d8270d5289ab20156f6675186473ae0f62b175369`

```dockerfile
```

-	Layers:
	-	`sha256:5895451e03148d40f2c534a11e2fc85be21f3589c3a5808d7976f8e8b0111965`  
		Last Modified: Wed, 03 Jul 2024 19:22:51 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json
