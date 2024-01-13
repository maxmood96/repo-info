## `docker:rc-cli`

```console
$ docker pull docker@sha256:57a149da1dcd999737a3aae3ed00bdcc50465aa35b8e3ad7c017117c736389c8
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
$ docker pull docker@sha256:a9781f7230f7d71d6d9d96f93d406f78bad47f7aed79905edcbc626829a915e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57690961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbeda2e13bbd502e2ddbec0ac7e60a6d16b5f7f3777ebf45529a9eb4df4a523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_VERSION=25.0.0-rc.2
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64'; 			sha256='43fb39c0bc24ac796123935032eddcfb57a7acd9216badeb10714c986ea1e090'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv6'; 			sha256='cb407cfd396892cc0317ef48570492d7e59445a9f50e92181fdf637548801d55'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv7'; 			sha256='936b474e24a51a51fd797bd18290da6abf72d62a614d8730a1fed3deae816ed5'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-aarch64'; 			sha256='d23d03be5880a2f6555932c572ddbc87bd0e1c4c1985933b7488d948eb2494ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-ppc64le'; 			sha256='f52678e23b143b26c2ee20af4ac105ed571bb2e8e39d59478e04bd2d81cbe27c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-riscv64'; 			sha256='555a373414675ae21cafff8280346c94561457f4be254b5576b22f4b5e8f2ab2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-s390x'; 			sha256='37871d879aa0a73f2ac59dab9805bee751d25208bbe72d7d2ab45956f2e1750a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 13 Jan 2024 00:58:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b7f064c01b1bb00930b3e01703d33a3722bc48570f05caabe254fa622d5b11`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 2.0 MB (2018470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384ba132479eeed7dc2a53d25983e63aa3f6154460441fdb1a3e3f7a80443e7`  
		Last Modified: Sat, 13 Jan 2024 01:55:52 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925fa9b01434370f38b386a384af6d0cfac8d48915687812313cb0ac0a56d2bc`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 16.9 MB (16893464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b7ecf52b17acaf42aea5c9db0fc3cf2c7200d2decc8772147016efa6ae5b5e`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 17.2 MB (17195298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2b37a68e23c28aeb3a824f509fd6aa0af4e44a8c13ea0dc404eaaccc8f265`  
		Last Modified: Sat, 13 Jan 2024 01:55:54 GMT  
		Size: 18.2 MB (18172990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29174eeb0beb2d30a18ef5f97f20708774acd7dda13ecd162ac8031642859f54`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f70c9f92f25c65b317150b377ebe33464f21796e7d63465db037d357623426`  
		Last Modified: Sat, 13 Jan 2024 01:55:54 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34dbdd19712963316234ef84221fcbddf7c9adc6ec9940333d65beb0ac06407`  
		Last Modified: Sat, 13 Jan 2024 01:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d443a69c38a8d68683c3fddba9e7b5d9cdbf31d3824e8793b6b012a57b840287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.5 KB (392492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c03d542140cb9e1ff5bf43c60cac198d5f8f319d392cde6aa8fb43a0baf19f`

```dockerfile
```

-	Layers:
	-	`sha256:9f6ce5e5ecf137915813c4b162bae4632730a8c7735cb6f5c345ead7d61923c0`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 354.7 KB (354658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e3032b47fd23646674d0c81e4754144d7130d8e103b003659279f651e352d9`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 37.8 KB (37834 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:e5b086163f906b877d58edd1bda1a1dfbda296d8a8fe6d29d3c2507c6b2da972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53515915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fefb216519820807533c5eb11ec1e1c30f5c29cdff7d6db461fcab18a9c469`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jan 2024 23:39:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc5bd010434069cd814513c40515b0b34d950c4606c108f726b20bc580362b6`  
		Last Modified: Fri, 05 Jan 2024 22:45:12 GMT  
		Size: 2.1 MB (2108662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbc809bdc4cc776e79e9ae1a93a9fed1e6438a007c9fc5f7a92f34cfbaa9fb4`  
		Last Modified: Fri, 05 Jan 2024 22:45:12 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e7897800cc2b23d3030b1a9c9173221d94fbfd649f6643e6f428be9639891`  
		Last Modified: Fri, 05 Jan 2024 22:45:13 GMT  
		Size: 15.3 MB (15272357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2be037f240c46b517059dfc837e61eadfa5731635a07e17819bcf0ac3f4ea0`  
		Last Modified: Fri, 05 Jan 2024 22:45:13 GMT  
		Size: 16.1 MB (16099979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1ca3f10014f10b5cdd33ff8cdf4de8f378e56e418d3795d19ecd700d4f700c`  
		Last Modified: Fri, 05 Jan 2024 22:45:14 GMT  
		Size: 16.9 MB (16867515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d650cb03a5b17227a94641ef1f74ee607e6748f45163181dad79ef9f370f`  
		Last Modified: Fri, 05 Jan 2024 22:45:13 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aab55d6b8bf19872ae330d7cd51284a80e096a8256d239f80d438eee2bb7a23`  
		Last Modified: Fri, 05 Jan 2024 22:45:14 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1880538cdbfe82434cf137f1293dd225d341b160de4c7bbee6373be585798992`  
		Last Modified: Fri, 05 Jan 2024 22:45:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ee7c8fc74b2d9c3ad3ba10e53bad5969feb0a063ed2b32da059ca83551802f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ded59b767f0a9bbaf8968fea5954db70aa34ec07e928223bc1593899037bc7`

```dockerfile
```

-	Layers:
	-	`sha256:83a72b9f8533b17f1de75f86cb1cd88f738e55ade234d8487d3d23d83a1b9bb2`  
		Last Modified: Fri, 05 Jan 2024 22:45:11 GMT  
		Size: 37.8 KB (37767 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:22d5e41e55588e9ffa2402e26bc7705e3f5976291356a7f2248972a7d3b2fcfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53011805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a47e0c571fbd1eed0c9955ac0fb6ac922dc60069cbb55bfae0bedd04efab25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jan 2024 23:39:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
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
	-	`sha256:d1399c95d35da7a273502e48feb8e4fec31ab4fc53455657a7750ec6cb12dc7e`  
		Last Modified: Fri, 05 Jan 2024 02:27:23 GMT  
		Size: 15.3 MB (15265152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da9ff40d4366efb6a51826d6f9444748455e6aeaa7208d93fd17603cc5743ee`  
		Last Modified: Fri, 05 Jan 2024 02:27:23 GMT  
		Size: 16.1 MB (16084084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4197dabf6c1df3d0041e8ac9461e3ebc3309ae1f74cbcec14e228a73e767ee`  
		Last Modified: Fri, 05 Jan 2024 02:27:23 GMT  
		Size: 16.9 MB (16852960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07af02685d6e253b0f361dbf996995f3f0d4d02ee1d13e5ec61880b1e65f50df`  
		Last Modified: Fri, 05 Jan 2024 02:27:23 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837e93f9f247b771545427cc7216dbc2eb479966807f9728567172f1c206883a`  
		Last Modified: Fri, 05 Jan 2024 02:27:24 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41e66a9a8453c4655e6cde0761e0f7662efe2d8b45055e62bf4f720c041863e`  
		Last Modified: Fri, 05 Jan 2024 02:27:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3e08d6256429794eebae5b1c8b236be4e6eb2b823a947bf7c39c06c1c36546c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.7 KB (375698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63d5df471f5693abe60f2996c857dac596611eaae82c852dca8f15978976ea2`

```dockerfile
```

-	Layers:
	-	`sha256:fd2eb1b8c2f0295b492a57aaa395e5b1f77829c7df0b36b06e37331470622005`  
		Last Modified: Fri, 05 Jan 2024 02:27:22 GMT  
		Size: 337.9 KB (337883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389e6e68014162ea10a9e9c898fde62bab0a93112ecaa92ee3147e9cca26e838`  
		Last Modified: Fri, 05 Jan 2024 02:27:22 GMT  
		Size: 37.8 KB (37815 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d6d9fe164a5ebdcde6b9a051ac2027c165c86d6e7b40641d4fb649838779ff1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53514986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e2d657ff003d0760119c59376662e8ab28378ace31b0aee3f83cefb1853e99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_VERSION=25.0.0-rc.2
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64'; 			sha256='43fb39c0bc24ac796123935032eddcfb57a7acd9216badeb10714c986ea1e090'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv6'; 			sha256='cb407cfd396892cc0317ef48570492d7e59445a9f50e92181fdf637548801d55'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv7'; 			sha256='936b474e24a51a51fd797bd18290da6abf72d62a614d8730a1fed3deae816ed5'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-aarch64'; 			sha256='d23d03be5880a2f6555932c572ddbc87bd0e1c4c1985933b7488d948eb2494ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-ppc64le'; 			sha256='f52678e23b143b26c2ee20af4ac105ed571bb2e8e39d59478e04bd2d81cbe27c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-riscv64'; 			sha256='555a373414675ae21cafff8280346c94561457f4be254b5576b22f4b5e8f2ab2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-s390x'; 			sha256='37871d879aa0a73f2ac59dab9805bee751d25208bbe72d7d2ab45956f2e1750a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 13 Jan 2024 00:58:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
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
	-	`sha256:ac9ce9355c7eac1b612e968f40710754b6f67908ba443da9fdf04e8ffeeb9418`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 15.9 MB (15901428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8868d84a8d0f0227f035dfc69bf4d0b7fb5dd196163d55d834724bfe8c4eca3d`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 15.6 MB (15640597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced2fea1225571c5444ed013200c3e5a448e255f93d62d524568e8eae99c5e67`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 16.6 MB (16608012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72ce2a51daea36c908727a2d1d6d0b5010b0c5930ac86b2dd114769b8433d9c`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5a1ab4f0bfc9487191e3c211da3ef8fbe55cccbe8c45218b48c74ad689827e`  
		Last Modified: Sat, 13 Jan 2024 02:32:53 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c04de793f9276bc0c4cc72a94991881f4c9159a54a67f62a240eb69440802f7`  
		Last Modified: Sat, 13 Jan 2024 02:32:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:09597ef3007bc7dd74c7a924738fa04568c0b5637fefd0582dc06b6c5d7c94c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.3 KB (392347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79da30997be2ad779cd4ac9d914704307a230e5f05e29ddd463f6ea65c6de084`

```dockerfile
```

-	Layers:
	-	`sha256:855915d3fe0312611cdb8065a02340acf94400f00cf5b5419e99c16133f2dbe4`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 354.7 KB (354669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d34ea3990b436fd111de67cc54d3a43c911ed06b8a693ebed11b6c15d876846`  
		Last Modified: Sat, 13 Jan 2024 02:32:51 GMT  
		Size: 37.7 KB (37678 bytes)  
		MIME: application/vnd.in-toto+json
