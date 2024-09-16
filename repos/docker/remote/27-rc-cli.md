## `docker:27-rc-cli`

```console
$ docker pull docker@sha256:f1e9506e0dc37103b3c827982bdb8eb1aa02b9daa53bfdd3743134c732d0a6e3
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

### `docker:27-rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:b3741e25c0a82e9367ec4a4f5223ddc3e8af7fb473352a121d938a021164c052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67535112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595be848766c00591077f3e01e7225d16703441918f97ba0076831275761f213`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 11:06:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Sep 2024 11:06:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 11:06:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3e8849902084f2f3fd785bcfe58f28f8835bf59f2f5b25a75ab0241d9d319`  
		Last Modified: Mon, 16 Sep 2024 18:57:24 GMT  
		Size: 7.9 MB (7872629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e18bbc646268feb8847c371dec884f69dbdb6cc6dd82d3d678a9f14b0b6e7`  
		Last Modified: Mon, 16 Sep 2024 18:57:23 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50787d2b4edf6b87ad6e93048056ca01afc83af44554b066f5e6999311c490a`  
		Last Modified: Mon, 16 Sep 2024 18:57:24 GMT  
		Size: 18.6 MB (18562798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9499ec5416c4d35c3c91bd4fa952cf81399f35669a0a05c9addb2074f10566`  
		Last Modified: Mon, 16 Sep 2024 18:57:24 GMT  
		Size: 18.4 MB (18437712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a3ab2bac037f17e5b70fa61bd1505dd41f2b076f27ecd50358b59e72377d25`  
		Last Modified: Mon, 16 Sep 2024 18:57:25 GMT  
		Size: 19.0 MB (19036016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca6043529f1d90d9198762a2fc42c643a2b8d5d5beddf93fae123e6bc1727a`  
		Last Modified: Mon, 16 Sep 2024 18:57:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af26356b05f6365c8d5f8bbc9202fffbaf0cf6893bdcdaba1dd028348c61625`  
		Last Modified: Mon, 16 Sep 2024 18:57:25 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c6e3a6117f962dfec48fd6240b6c794c49889772f0e08f2dbb8542001011af`  
		Last Modified: Mon, 16 Sep 2024 18:57:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e8bce05a426d74716846d9bb031645c2195764703aa0e26f59c04497e2bb053e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41725c78ab40e385d04adcffd2a2786de82e55aa7e60f3ea1fcfd38bbbe83dd9`

```dockerfile
```

-	Layers:
	-	`sha256:63af7911810d88ad71f5e4d26680b6cc37a341034601a0ada156c5005c8f3a4c`  
		Last Modified: Mon, 16 Sep 2024 18:57:23 GMT  
		Size: 37.7 KB (37710 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:7731db9c0771684d78f0cc4a3ac8f07285357a0db9507b560797cce02b154a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62805277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9bb53f86bcb1071eeb46a7cb1c7f0756bf7194a7155941060f13a4aa04b522`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 11:06:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Sep 2024 11:06:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 11:06:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37549dd8e6a6d0cdc996cc5449b22373bef199464d62afc97165e91bd4ce7194`  
		Last Modified: Fri, 13 Sep 2024 18:56:23 GMT  
		Size: 16.6 MB (16601245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecc51522c1dd8bec9e2a4dd04d57834bffc385d2118a77d5817edd2a634dbc5`  
		Last Modified: Fri, 13 Sep 2024 18:56:23 GMT  
		Size: 17.1 MB (17145035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b6b181b92406c5a225c1a5186335177947c9c64e4f89d543e4b788908073f`  
		Last Modified: Mon, 16 Sep 2024 18:56:59 GMT  
		Size: 17.9 MB (17882570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ec85b22190cc21fa991d16190d1a72984f6215979724007147fe4a92aa4ff6`  
		Last Modified: Mon, 16 Sep 2024 18:56:58 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640111c44b8febd5c7250d4913b08d22dc2fd20538f6237b24bb5fc3e0dc5dc5`  
		Last Modified: Mon, 16 Sep 2024 18:56:58 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fc652b165fc32ab1171f8ed82c8a4484d9a877a161c893678e7a32baa7466`  
		Last Modified: Mon, 16 Sep 2024 18:56:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c57c6f8a0a38be5406f34cb74ef03aa8e54e8a135e790237e39959058db9eb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d640405950800a369685f61545bb3aa35eb00104b253506990fc129f62a6000`

```dockerfile
```

-	Layers:
	-	`sha256:100c5690849cb1ba9e88e8d95d7c6df1c425fbd084633b45b14f6886aa785461`  
		Last Modified: Mon, 16 Sep 2024 18:56:58 GMT  
		Size: 37.9 KB (37858 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:39ac0195dde622cca63643cefaa483b7eb232534f37edc27e4ed3efa7d21bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61837262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56839d002ebb7b6f5524b3a1c9a5e83db9df317c4c102aa8a6fcfeb13e2629e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 11:06:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Sep 2024 11:06:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 11:06:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d3ee078c98df2b09361b18c3ef358e4394cd924061652a17793b08ddaae6a`  
		Last Modified: Fri, 13 Sep 2024 18:56:13 GMT  
		Size: 16.6 MB (16590994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db63cdca03f9525b3158778ada4971fca8f6fe02a5fcfc1b97ce3f0b93662f09`  
		Last Modified: Fri, 13 Sep 2024 18:56:12 GMT  
		Size: 17.1 MB (17135230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb265068a10a0cfb558fa6e1bd33dd1a88368c0f6da3a7231bb31a6d398d397`  
		Last Modified: Mon, 16 Sep 2024 18:57:10 GMT  
		Size: 17.9 MB (17869513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57936f988506d478cc8136aa66f4cd2a8e24cca57be15a89276bbebe3d62f04e`  
		Last Modified: Mon, 16 Sep 2024 18:57:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4ff6df1d38b9b04bb96025ad59959a0851347d05b2c4e11dbbc7375ab2d7f7`  
		Last Modified: Mon, 16 Sep 2024 18:57:09 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476bf6e22038ebdfd0bac2151f0cdb4f7cc2044323cdb139ca447cae52d42ea7`  
		Last Modified: Mon, 16 Sep 2024 18:57:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:023663f999ab5da84a4c43a5168e34595a70f64b5e3d7fb0469b239447766361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dcdebf0d870e3c11d52b5f23ec4b5e2724aa4c0c91310bdbf3b0b22e5bacc9`

```dockerfile
```

-	Layers:
	-	`sha256:6e5dd01ead07fa10a4499a6145a7af0ce78454e299a063e7494ce894ab7fd9d3`  
		Last Modified: Mon, 16 Sep 2024 18:57:09 GMT  
		Size: 37.9 KB (37858 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ad38c7a2a5d7942f8e9e280300cf6447083047cfcec33a2f451143bfd57e8acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63803040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff434da00016e2c86d7a536ba75473e2190a12c272a7c2355b22fb829799688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 11:06:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 11:06:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Sep 2024 11:06:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Sep 2024 11:06:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 11:06:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7ab6a65b5548b28c6ea479b5fa1d0e59628b777830db0afcafd60fb3ea2a24`  
		Last Modified: Fri, 13 Sep 2024 18:56:10 GMT  
		Size: 17.5 MB (17515930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e4860376f01b29ad074f91764ce3a106a4766d66e3c0a722484baa53bd66bb`  
		Last Modified: Fri, 13 Sep 2024 18:56:10 GMT  
		Size: 16.8 MB (16800754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bc06bbb608b659faa9cf501ca521a2bff1d6fdf0b1eb5ba639440eaacd3082`  
		Last Modified: Mon, 16 Sep 2024 18:56:52 GMT  
		Size: 17.4 MB (17414619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6614f199bee42d7d7b3d7dfee2213e58aff9315205b9fcc2477720b315e847c8`  
		Last Modified: Mon, 16 Sep 2024 18:56:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16659473e6476b5eabc21aef8600620379c9b3137e0621ddaea3e5f48235b2d`  
		Last Modified: Mon, 16 Sep 2024 18:56:52 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f17af642346b11ac3e8799b8da4d53595252fda7daaa3c78e124744c2faad9`  
		Last Modified: Mon, 16 Sep 2024 18:56:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9de6448a0222aa8f5553dc1269119f7e893ea47d75008e1335e697eb23a7e684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838aa0134440f6414143ed96d5b6f84918858d24ccd6ce29f8e342045323bf19`

```dockerfile
```

-	Layers:
	-	`sha256:075446b23885d954ca6ffcf710ff1a8a55b2de824dddc196529c2dc8b200b099`  
		Last Modified: Mon, 16 Sep 2024 18:56:51 GMT  
		Size: 38.0 KB (38010 bytes)  
		MIME: application/vnd.in-toto+json
