## `docker:cli`

```console
$ docker pull docker@sha256:0ba70143c704ac27099440ff763d8a1dfe75acc92ad3c16c9bbfa7fdde9cd2cb
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
$ docker pull docker@sha256:b77ba76d471e5c0963b2c2d0555fb7636e8727166e4ee0393a1c6ecd89b8b504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57694260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee25a5af8cc348592e903a590cc46fc3a6de95405cc41afc49d4eeb34ac89420`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Mon, 22 Jan 2024 18:05:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENV DOCKER_VERSION=25.0.0
# Mon, 22 Jan 2024 18:05:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Mon, 22 Jan 2024 18:05:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Mon, 22 Jan 2024 18:05:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-x86_64'; 			sha256='067a12983b9333d01947329190af756b6d12afe7b4b51b3e1e29328b4afe3b9f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv6'; 			sha256='582d734ef0c14335ee4691f3550d56b3e1c1c4d787ed6354830b3c222eee542e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv7'; 			sha256='e83fa84dc73cc8d5a0fe2d1ad3ad61202050f033e6df9f3f4f7b3c2b59181006'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-aarch64'; 			sha256='beafe762fedd06fe9885317c33f8b29b39c2354d6840a494a69b3c3a36919212'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-ppc64le'; 			sha256='6be73d6597efc822eff3f9dd6abb56b72ada76f8a5f798b1df2dce5105f39257'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-riscv64'; 			sha256='33a15fcef9d975aee4ed404779fae068264da6de8f2851ead85f9e1701302411'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-s390x'; 			sha256='0b62a8d7aad7ce81220a4d77aa4b17e443b888248c1da22bc808db1fcbf1e9ac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Jan 2024 18:05:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jan 2024 18:05:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99fecc646a5691be8226c22d5248cb6f9332cdd8d03b2813a53923bb6e1877d`  
		Last Modified: Mon, 22 Jan 2024 22:50:02 GMT  
		Size: 2.0 MB (2018465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893d3febe591f94c7054aff6f650f5c5a44dd86d2559ad91aa401eb51c9b228e`  
		Last Modified: Mon, 22 Jan 2024 22:50:01 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc11cf79467c2396782fe79ab0dddcb2a4651a129d862c10736348a3bb90676`  
		Last Modified: Mon, 22 Jan 2024 22:50:02 GMT  
		Size: 16.9 MB (16894259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c541db7b3bb6fda7809dbe93d93ca00685baf5e9c554b213ccd9aace6368ee1c`  
		Last Modified: Mon, 22 Jan 2024 22:50:03 GMT  
		Size: 17.2 MB (17195294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802cf11ebfb4ba794cfb0c613511bdd6927ddc13a20660c78be4790e8f4da5f0`  
		Last Modified: Mon, 22 Jan 2024 22:50:03 GMT  
		Size: 18.2 MB (18175508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05773fd6f3c0c28805bb9f2d6d586fef02c44d0cf25f8e4eb296c1b33a99655f`  
		Last Modified: Mon, 22 Jan 2024 22:50:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886efdf86c556b40e0929438c85d489fde709389f6e4d70099ce9099e94db6a8`  
		Last Modified: Mon, 22 Jan 2024 22:50:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1604244e76aac43af382a2eb7d7e4d4440c35114f4f2fab0865d9e29e21e6ab`  
		Last Modified: Mon, 22 Jan 2024 22:50:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:bcd51b2d380cc78be4d6725729986c88f3ad6e8bf18cc3f207a2354af823c56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.3 KB (393321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783cb49d257d8e1291d9e3c9fd94073dfafb4bd365ff9c221c597402003146f9`

```dockerfile
```

-	Layers:
	-	`sha256:966d3bfa4c859c6f97ca1947f69ae70fd649d820894836f82bc28e99df37954c`  
		Last Modified: Mon, 22 Jan 2024 22:50:01 GMT  
		Size: 355.3 KB (355278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5cae4c2e3815308166a6e4e611c6cb076eb1f1a5d5d18189b98e0b8ee98714`  
		Last Modified: Mon, 22 Jan 2024 22:50:01 GMT  
		Size: 38.0 KB (38043 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8df3dc705e6bd816a3d37826aa5e38c19932eb7e37fb2a08808ab70bf9099900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53821863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97096ba4b99ee966aebf2066ca0b49f16bd6f28da8450bcd6170874ac9a94c2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 18:05:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENV DOCKER_VERSION=25.0.1
# Wed, 24 Jan 2024 18:05:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 24 Jan 2024 18:05:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Wed, 24 Jan 2024 18:05:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Jan 2024 18:05:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2024 18:05:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441706b0b6a79717692c9778c5f50078980694f27e12ce415b2197836c0b2121`  
		Last Modified: Tue, 23 Jan 2024 10:53:06 GMT  
		Size: 2.1 MB (2108638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274588671fecad1a12373b82e5dc2aca58048bc38e5d3f037db38ade3324925`  
		Last Modified: Tue, 23 Jan 2024 10:53:05 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aa34887b19c06be9c0fd793e8a487e50e0db82ad6f0700de7c5f686a60bae3`  
		Last Modified: Wed, 24 Jan 2024 21:00:03 GMT  
		Size: 15.3 MB (15271637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aae634e551f4736a74e0de8fc4011565d66d3d8a1c9e84f1af35468fef9fe1`  
		Last Modified: Wed, 24 Jan 2024 21:00:03 GMT  
		Size: 16.1 MB (16099986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160beda2422a41cb83a1fe1bc5737e88a05a57b678c0ba985315ba6a6086483`  
		Last Modified: Wed, 24 Jan 2024 21:00:03 GMT  
		Size: 17.2 MB (17174203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e9e34791805d0be4f7e2b5fd94e2b2304af5d692969c317bb8cb664dd3bd8`  
		Last Modified: Wed, 24 Jan 2024 21:00:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae575d29b078bf67f2390a42519e6438551301702b7e8a507a4ad34863e1676`  
		Last Modified: Wed, 24 Jan 2024 21:00:04 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3f8d547eeaed3c119d75baf3f9ccce27793d74243bf69b7bbf8e4e638c59b2`  
		Last Modified: Wed, 24 Jan 2024 21:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e6e2cd551a8ee61dc172836e5d5e2c6bd69e010f0217647d43da725d8eeeee4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648d05b25f07abd286075fcdccd530a9507e86f1983dafe197eacd90df0f3139`

```dockerfile
```

-	Layers:
	-	`sha256:ebe6d0c3f5bc4a8b3888b77ae76b27c95338a440842332aed7d142b7f0800af4`  
		Last Modified: Wed, 24 Jan 2024 21:00:01 GMT  
		Size: 37.8 KB (37817 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:fec3a03952c9057d013df16bed2b5a056abf6a1496308cc00c1967933123ea42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53328652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60156ced4ed7ffe9f7b118ee719c563819820a1b4051fad1f91ee725cdb6f755`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 18:05:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENV DOCKER_VERSION=25.0.1
# Wed, 24 Jan 2024 18:05:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 24 Jan 2024 18:05:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Wed, 24 Jan 2024 18:05:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Jan 2024 18:05:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Jan 2024 18:05:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2024 18:05:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7102b17e4ec828559672f3388bba1ec86d87e7aa09caba4b82fc6870b4fa6`  
		Last Modified: Thu, 14 Dec 2023 22:03:12 GMT  
		Size: 1.9 MB (1888652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f19fa8a6c45d74eb65c7d5844869fef846c8305dd15e21604b2c06e20d1279`  
		Last Modified: Fri, 05 Jan 2024 02:27:22 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f55303c45fe6e4ceb7ded22a5f4ec82d6e3b944ff5fd0e34e946c243b5516fe`  
		Last Modified: Wed, 24 Jan 2024 21:23:33 GMT  
		Size: 15.3 MB (15267848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad337070384e9cdad75d659ecbb01b57477deec88cdb8930ab1957401a603510`  
		Last Modified: Wed, 24 Jan 2024 21:23:33 GMT  
		Size: 16.1 MB (16084092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17194f54b764ad754e9cc7416d766f62d8453e0eb079aa81d2ce25b3fecee940`  
		Last Modified: Wed, 24 Jan 2024 21:23:34 GMT  
		Size: 17.2 MB (17167101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74638158749a678b151340fe7395474f1359c91bfaa3dbb267feb61f1aadd6c5`  
		Last Modified: Wed, 24 Jan 2024 21:23:32 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a740ec1e118a9ce8469d40e651a926ed6527c2e831484696aaf10b598cfd262`  
		Last Modified: Wed, 24 Jan 2024 21:23:33 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa26e96e66e48f6a9b5ed79a0e180d47d01af19a94bf6d5796b93275d4895d30`  
		Last Modified: Wed, 24 Jan 2024 21:23:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a700cefcbf26c4cec20c0f223508405b4d5950fe16f8ff9e6609f4eb5803524c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 KB (393352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf259aa4732e3e7d96e183bba88a463191b73b1d470b2572b54bb41a2fa45ef`

```dockerfile
```

-	Layers:
	-	`sha256:ad3454bf47756227e1013d5fd49866032f5a9ba21db676dbe4a9d78fa5452961`  
		Last Modified: Wed, 24 Jan 2024 21:23:32 GMT  
		Size: 355.3 KB (355321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6667e452f2f9d309c197618aa70423c10e907ff94f1640dd3f8d914d1322eab5`  
		Last Modified: Wed, 24 Jan 2024 21:23:32 GMT  
		Size: 38.0 KB (38031 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:85444f047201398bd210546de1bed814a8d319356d96f7f0d0230d2c898ade10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53514675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdc634ad41648e6512c2d69cc91cd5f9c699643ddf7eebe87e3853dcd2b5ef5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 22 Jan 2024 18:05:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENV DOCKER_VERSION=25.0.0
# Mon, 22 Jan 2024 18:05:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Mon, 22 Jan 2024 18:05:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Mon, 22 Jan 2024 18:05:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-x86_64'; 			sha256='067a12983b9333d01947329190af756b6d12afe7b4b51b3e1e29328b4afe3b9f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv6'; 			sha256='582d734ef0c14335ee4691f3550d56b3e1c1c4d787ed6354830b3c222eee542e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv7'; 			sha256='e83fa84dc73cc8d5a0fe2d1ad3ad61202050f033e6df9f3f4f7b3c2b59181006'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-aarch64'; 			sha256='beafe762fedd06fe9885317c33f8b29b39c2354d6840a494a69b3c3a36919212'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-ppc64le'; 			sha256='6be73d6597efc822eff3f9dd6abb56b72ada76f8a5f798b1df2dce5105f39257'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-riscv64'; 			sha256='33a15fcef9d975aee4ed404779fae068264da6de8f2851ead85f9e1701302411'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-s390x'; 			sha256='0b62a8d7aad7ce81220a4d77aa4b17e443b888248c1da22bc808db1fcbf1e9ac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Jan 2024 18:05:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Jan 2024 18:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jan 2024 18:05:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4959de38143abac793d31e4e8592696721305ff06281f8b9284aee380afcfe`  
		Last Modified: Thu, 14 Dec 2023 22:04:39 GMT  
		Size: 2.0 MB (2014899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf613c8d3eefad31faacee38beeedf68069e48ea01d8f083fa0a57ce343ed827`  
		Last Modified: Fri, 05 Jan 2024 02:15:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594895876a66f55998b0c3d9c175ec0cfa723898879d7fe8f837de3b0e9e01e6`  
		Last Modified: Fri, 19 Jan 2024 20:23:15 GMT  
		Size: 15.9 MB (15901598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5598890badaf41ad29ca6e7a62aecf9b18e64ff1308118644d6ecda191bee6ae`  
		Last Modified: Fri, 19 Jan 2024 20:23:14 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08400fbc822ec742c74feaa2c8ada0afc029515edf89fec4102a3aa26dae8a3`  
		Last Modified: Tue, 23 Jan 2024 01:47:07 GMT  
		Size: 16.6 MB (16607523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634b0bcb9abfaa96af63dbdfd8e366dc9b1fbe0de8b906c4d9d312e5f90418`  
		Last Modified: Tue, 23 Jan 2024 01:47:06 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7303addcbef4ecd329f524a7931a7c0856d5c284f751716ef9934dff4462b8ac`  
		Last Modified: Tue, 23 Jan 2024 01:47:06 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc13d7fb096bafcb15abbc0caa3609ccd8976bd665c9d1b526968be6a672c0e`  
		Last Modified: Tue, 23 Jan 2024 01:47:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0597c3c611be0ea4d4784bb66d05f9a532ef8245e05571609b7f9a4394bc1bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.2 KB (393180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3194d0c4554972aac454bf61928e890470aec1e944242c18b3af78b3f4aa4e`

```dockerfile
```

-	Layers:
	-	`sha256:4b97ea814a101fb7fb6ce74ad5362d282e1b3aca47a4dfe203d89ba632239a3f`  
		Last Modified: Tue, 23 Jan 2024 01:47:06 GMT  
		Size: 355.3 KB (355291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4842edf357ce9fb16fd6132c34675bb9cb9a2fd6ca2a4c90cebce513ee4a586c`  
		Last Modified: Tue, 23 Jan 2024 01:47:05 GMT  
		Size: 37.9 KB (37889 bytes)  
		MIME: application/vnd.in-toto+json
