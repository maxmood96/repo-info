## `docker:rc-cli`

```console
$ docker pull docker@sha256:c40e46d9e3324ca8f7534a00547f10e9f6f3b3034ea8a4880969f328cfd7fad8
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
$ docker pull docker@sha256:a39da33fdefda06d837c14e7a589966ba1e9f93cd9b32bea90e2fe89f5607ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57739303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4f535a37e493f4454a815a45f137ac581bffa5c2cd9e9961add54ba3c0c9b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a0291d2775c9c58a81d97c0a6ee6d7456f9dcfb53274d8394c29d8f32ef1b`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 2.0 MB (2018448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0a6a69c9223cbeac96a98d829b7defd1198309e4c39e7530ee337d4889b1f0`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a8e00b723ec9b1c002c2dddb8a264ad57cb559d35a37668e764d7e88e274b2`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 16.9 MB (16906057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad9dfe6dcd75b86ed5b9ddd8d9766723fc222fd596bbbf3f1d56c777c7dbcc`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 17.2 MB (17195299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680582dd5f6748caca89d3f4149ae100db56f6466396ccdf32ece2546deddb37`  
		Last Modified: Thu, 29 Feb 2024 19:49:03 GMT  
		Size: 18.2 MB (18208514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5339634a3f121e1cb897e888209eeedd655a8fec1645dead6162d5f619fd27`  
		Last Modified: Thu, 29 Feb 2024 19:49:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3966f289c893f3596bba3677432bb6c2a4cf1f2fa9983ac4d1a940ce9089d498`  
		Last Modified: Thu, 29 Feb 2024 19:49:03 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99726b899005908fad4b410e2d949e6fc4beec7aba1a3105662e60d30765c9`  
		Last Modified: Thu, 29 Feb 2024 19:49:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:180247d660f984f7c5f26a90f540f64a3f6a9ea8f88484fe12c0ec6af840fa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.2 KB (428193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a4cb8c7c84e758c3797517fd5a1d5d120b95075f3a7ddd3ceffec238b5d197`

```dockerfile
```

-	Layers:
	-	`sha256:94ee23d65483c3fc0da3a28d0b9682d40c4b75061f08fb583fec68cef3953f1e`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 390.4 KB (390375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d8cff1ded56e7121caf41756f38eb293c3069e386359286e36ce40c25b6fb0f`  
		Last Modified: Thu, 29 Feb 2024 19:49:01 GMT  
		Size: 37.8 KB (37818 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:545c1b4dbe48e8bdcbcf29b8cac7e7cfd3e58daf0f64a7eec251c3b44ded8ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53820099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b3184b8d145301648e169650a008bd2b2b46077b60b6b51d87dbf471b03958`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 12:12:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Thu, 18 Jan 2024 12:12:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 18 Jan 2024 12:12:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Thu, 18 Jan 2024 12:12:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-x86_64'; 			sha256='d350bbbd1c74c0a8542193bd41881afea534b141c6a9d9a27b2f217e51d5c48c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv6'; 			sha256='4a89b48f6a758793d4b40b1ade7bd9e7e2e177e29f05f74abb3fde08f246f0c8'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv7'; 			sha256='2b339b900447394b0cc985d9be30782361828b615ce743c36a9674d4435a2fb9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-aarch64'; 			sha256='9b35494742cc54544cd3f67b162ebfb43435077f02556bfb5a7e1c543f0a2da7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-ppc64le'; 			sha256='68ce36587759f18a9daaf4a11af6db1ba9e4b7089a8062654de38f8b84506647'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-riscv64'; 			sha256='b28cbb99ba1ae9d7b1a4e5d6828a2c2a9b124db2d4f1d226aa71a1f2741aa056'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-s390x'; 			sha256='6177f40328d4004d37b7e422d102d765aeb03e24e202ca8b791a6c000be90665'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Jan 2024 12:12:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Jan 2024 12:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 12:12:51 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37591cb9dd2cfdfca65b178b489c279ddf98c80db713614ebfb00d8a06b750d1`  
		Last Modified: Thu, 18 Jan 2024 01:07:50 GMT  
		Size: 2.1 MB (2108664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f528fe69dcb5a3cc27e1506619594dc932046c740bf0f8515eb8903ea27eeb2`  
		Last Modified: Thu, 18 Jan 2024 01:07:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f29e7c1e6b71fe0b086d3ff7a5f4a0a77035ed0c69cb591c045718ff0722a1`  
		Last Modified: Thu, 18 Jan 2024 01:07:51 GMT  
		Size: 15.3 MB (15271662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87f71dbd2c565f1b5185d96b8bc8236703dbf2e40704dc77ee81692433e5d3`  
		Last Modified: Thu, 18 Jan 2024 01:07:51 GMT  
		Size: 16.1 MB (16099967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec137b52143802bd0182bbdc6e7179c81ca3bd663ee33f416565b50582d07143`  
		Last Modified: Fri, 19 Jan 2024 00:06:39 GMT  
		Size: 17.2 MB (17172401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68236f4affdea05acdeb4717394d216bf898c12b29c98f61ef83670184fca1b`  
		Last Modified: Fri, 19 Jan 2024 00:06:38 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d298071b11ff7d1f0a923b08236e654ed2ac48dc57a79f8f08e99bc9561de61`  
		Last Modified: Fri, 19 Jan 2024 00:06:38 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d48a806856da2d55ddce34d3a3a4179574485a240b87e29ff866ebc5be62df`  
		Last Modified: Fri, 19 Jan 2024 00:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d06ba593857da18fb928ac0aee7d8bd97669d0d23fbb2d1e5e77fee3fd2d67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5086553a1f3ebd14b94bd39e73f4d8067b2d461c25c95713cd8416eb4ac1b722`

```dockerfile
```

-	Layers:
	-	`sha256:6460700748d1bd13d364475903016b02fa813151a050c2b71bf721f9a717acb4`  
		Last Modified: Fri, 19 Jan 2024 00:06:38 GMT  
		Size: 37.6 KB (37601 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:31f7057ecca0f9e4e9a19676f7bc714c38e826cd9506269a441a82bec1764afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53370609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc9ad15b8b306a29f8018e0d29957cb877fc1130e7d44919c033b3043801a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d7567cea9b984ed5ef416f6b88dae89cc6ee911a3c07a56bec9cb5e3db80e0`  
		Last Modified: Fri, 02 Feb 2024 14:52:46 GMT  
		Size: 1.9 MB (1896180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5f991740564aa851e62aa9c5fcc779094c0abfbee45897b4eefb30712b6112`  
		Last Modified: Fri, 02 Feb 2024 14:52:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f446d1fcdf6f1d2402c6a66491f645dac10872bc077665208524b76f7fd271dc`  
		Last Modified: Thu, 29 Feb 2024 19:52:49 GMT  
		Size: 15.3 MB (15276517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e126eed09001967a46e7d9367a84df25ee8fc3c4002fee5bf9e1af991e964a9`  
		Last Modified: Thu, 29 Feb 2024 19:52:49 GMT  
		Size: 16.1 MB (16084099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4cb4235dd696bbbdc7a674aaa993c40b26dbdfc9ad2de2b062912b051552be`  
		Last Modified: Thu, 29 Feb 2024 19:52:49 GMT  
		Size: 17.2 MB (17192658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea23fed4bddf5361d8a2c6c8f89a7d242b8faa7d38c766f707b33c20dcfb0f7`  
		Last Modified: Thu, 29 Feb 2024 19:52:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c7b35515f08fcb859a457ba884ab1c4d8086b5dd1f8b0c2b12c2eb6de83e1`  
		Last Modified: Thu, 29 Feb 2024 19:52:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09cf27233236b232b802f90f0824150af68cac97d6295b522d3723660da6ac8`  
		Last Modified: Thu, 29 Feb 2024 19:52:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9db2dd6e93890631c81e1996a4952dcc3a39a429502a623b09f7c6363f345a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.1 KB (428102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a664c8613c55e957a031d897b4cac346af8eca32be2232c6675424b237de5ba4`

```dockerfile
```

-	Layers:
	-	`sha256:c0d73e882d6762bc5c8a0c633d8e7d661be417219507c075748b78185efc09d9`  
		Last Modified: Thu, 29 Feb 2024 19:52:49 GMT  
		Size: 390.3 KB (390303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3368b79ae4ecdcce5056b517e50bb9dfaf12ca81aabe9fb5ad4af0c9dcdb33f`  
		Last Modified: Thu, 29 Feb 2024 19:52:48 GMT  
		Size: 37.8 KB (37799 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4036b16acf3de7b38f93cb557864ed2beb688f420a9a34471e332986cb681a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53567770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec58976b13868ade3f7284ccc5a0078985e0df7dfe63e6801bfdd8aa1ac19f9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
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
	-	`sha256:d5e373947c633ebf3fa9986ae70a2fd71f8df3215c7243e45124c067fd4548fc`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 15.9 MB (15917020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175757f58356331e958899b4d5e45a3f2b639ddec46c4cae57a44741ac538201`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657ac24788fe05605b760abd9d5b9b1fc663c92de3870c60805b00c0e29709e8`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 16.6 MB (16640489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68660a4b8ae70fc6a495d7eeb9dfa4fe01328afae2cd6d9fc914c73c48ecb5da`  
		Last Modified: Thu, 29 Feb 2024 20:00:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838e1329e0d77349ff18111bf4a7f447953856f6fa0417674c5ff064a513d830`  
		Last Modified: Thu, 29 Feb 2024 20:00:14 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3860585275b2dc666f25566e11b743ea4e441382777b0b808df04ffb5599111`  
		Last Modified: Thu, 29 Feb 2024 20:00:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:05c56535cf34f8730a6618927db557d2420761f3941be389be5b925b35ca7a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 KB (428048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b7daeb62c9d59af7fc8ce09480482512d96355c8b91b502ebb5e7b8c565ddb`

```dockerfile
```

-	Layers:
	-	`sha256:a43c1b73a7afc0145b3b1e28adef3f2e3e64c9d71f46b2b50db5a68b595e68b7`  
		Last Modified: Thu, 29 Feb 2024 20:00:12 GMT  
		Size: 390.4 KB (390386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b92c759551bde69da1968a6dcb1a232d42c474a82026c489bbb3b9295b6334c`  
		Last Modified: Thu, 29 Feb 2024 20:00:12 GMT  
		Size: 37.7 KB (37662 bytes)  
		MIME: application/vnd.in-toto+json
