## `docker:cli`

```console
$ docker pull docker@sha256:3486a702666745d124e1cd4452fb54d83789f735de9cedd4069d9d502065f692
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
$ docker pull docker@sha256:f2801be3440b90450aa31e12b2eabc05c25e73121f94a5d586561a98746d1bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8a61369db9e638cfb70d258507387d7e7e1288e3cf40cf073d741f30f5a9ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3439df56f15f001225f48ac742a303d0ad6b881adc274c1f1f5545c5aa9a`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 7.9 MB (7889558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b05996369ea833a1a88eff3d5e71ef0c7c790b39c791ffe616ce42c88fac0`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22347c48b0c1bc72a8119f60d5a52dede3317aec2218fd90d22e615970e1f`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37e3c56f09b6c0ca73bd29db36553bd0d0a626e89ecc5113e8a2353c62570`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a61ae0bb2d8ca58f35fbe7b44fcb26fb915709e9096f04d02a295a52f8486`  
		Last Modified: Tue, 05 Nov 2024 20:36:03 GMT  
		Size: 19.1 MB (19117546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7bccb56ed884750bfc838c8156cbb820025846d77b331a070dc32d11cdb74`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e65772fe7e2de9b986f6c2d2774d57443e13517b244806d44097f0e844ee9e0`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb536adbfcef83f20a6b21f6f56ffde6f98cc04659123cac7e2a9f0acb7361df`  
		Last Modified: Tue, 05 Nov 2024 20:36:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:45be58be6dc9dce5fa6181734a506c8901659c7956b3af5bff59692dfa7571c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7d61a68d868262220d2ca3efde40f5b4727014938e45dbd0eaeadac1547fc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd20cd91b5aebf693c5fb38d516f8016562bc6ff4272e1502c5c97af59c81c6`  
		Last Modified: Tue, 05 Nov 2024 20:36:02 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c95debe39252628ead592962bb624ff131ef6054aee786b9f1166656636c4485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62009875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eb3dd47ab956b4a4ec0801db472cb508d4ddc4fd91aa947fdb6234651b2185`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f36195754da77b07f990c05f9d9240c1563167d5e44b39c34b635eee1ae26`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 17.9 MB (17940720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686a480b39586ae8ddb6eb33b336895b2f040af93198e30523e066123ccfd23`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42b2d07793b24536a2944879e29cc347cc95115c94d6000ff56f2394146f48`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb2f200635a6b1874bc8140b7ba981fe472b91d688dbd6625a43898e6b6a2`  
		Last Modified: Tue, 05 Nov 2024 20:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:ab2a4aebf76b0f25badf4890a867c426814d31ca137a9fb448d549bbb3c39b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9ff21d60f9a42c750a9a43cf64ece7e7baba14a6d24a25306daa18b112d1d1`

```dockerfile
```

-	Layers:
	-	`sha256:381e55a3ea7f67fb99e65834af6a60bd686e1bc4634eb6f20c7bb3cea230a9b6`  
		Last Modified: Tue, 05 Nov 2024 20:59:04 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3742107db033a0ffe2044234a11cabe31f22d7622ed871b2964ce8e0178c03eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c894547a0ed403ca7cc8aeeb96fccf25556de38991be54a3ceb59ddc45d808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:753e957b7506c34733b986aa67bc6d13290df89cf35ac3ad29c58b67b85c8fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b67c22bb984bef0b64a776a355e40b269d6eb6208e0af05f6b97227532756c`

```dockerfile
```

-	Layers:
	-	`sha256:4ed4997071d9da3e39103f4860d9db8374d263ad750704346158e75c0634890f`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json
