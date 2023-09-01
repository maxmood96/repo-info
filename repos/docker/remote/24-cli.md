## `docker:24-cli`

```console
$ docker pull docker@sha256:21d8477f7dcd514414b1ffea6670d9963f0c81d23303452bb3ad7f93fedacb64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-cli` - linux; amd64

```console
$ docker pull docker@sha256:66fd3352871576395f25b23ac8a2c2a4d503ca43ea81efd9d912924489cce2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57094132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c502855bab44eb998644c302407cbbcebfb6dc2a6d9c892acb00c412ca1902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 30 Aug 2023 23:06:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENV DOCKER_VERSION=24.0.5
# Wed, 30 Aug 2023 23:06:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Wed, 30 Aug 2023 23:06:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.21.0
# Wed, 30 Aug 2023 23:06:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-x86_64'; 			sha256='08e549924823e97a3ea303c2309b812dfd5223b8be5ff96fe41bf75181ce0977'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv6'; 			sha256='058ec96bc81ddeb317d160a6dea5bd8ac65dc2e90afff86bcc31f3f818f3fc5a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv7'; 			sha256='d46dbbbf5723c45125277c7c75b757b22679962707b2276a6d52f35964583c42'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-aarch64'; 			sha256='5daf8d1a04cd649ad4a64221d0ca0cffcce33c740e60d5b15698545ce6d0436b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-ppc64le'; 			sha256='fadbb72890d72f1246b213c453ec90cf494f4f8ea3dda2f63678de53a7e97c15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-riscv64'; 			sha256='cd01536476864bd97c6ce3dfd317730535e51b2e252e9468de0379cc84298187'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-s390x'; 			sha256='dfa8ab3ccc83311a2a4fddc43654de06c13cadc7caf629a0ddeceabd24bb6308'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Aug 2023 23:06:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Aug 2023 23:06:33 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ac87b2a727c4c5eb8ee9d1f3cbf1df239ca23abafeae9063664206effd46c`  
		Last Modified: Fri, 01 Sep 2023 00:50:56 GMT  
		Size: 2.0 MB (2014286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3b0f7713d74440f758920f806604dc18003428e40c3adfda95ddf176663025`  
		Last Modified: Fri, 01 Sep 2023 00:50:57 GMT  
		Size: 16.4 MB (16390651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbab7b71df77ab8209d6010cd468cc0466afd60250f78f9e51bacc857d4e21df`  
		Last Modified: Fri, 01 Sep 2023 00:50:57 GMT  
		Size: 17.5 MB (17459273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7115b760bf892077f958365d78ecee5bc1b2a945336a0987f6648a266a1cf769`  
		Last Modified: Fri, 01 Sep 2023 00:50:57 GMT  
		Size: 17.8 MB (17826604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb33fbb55f1a2f4c4727afaf80cf10ec6af383a2beec12437d4b75e6cde4be61`  
		Last Modified: Fri, 01 Sep 2023 00:50:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fbbdffb8e345217b129c74f11cd8eb4e954c9e99586444d271acdd729e2c30`  
		Last Modified: Fri, 01 Sep 2023 00:50:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fb24f75fb015a50686f8ed2a930ff0792e4c58a6c9b8c55ff4f57a06dec820`  
		Last Modified: Fri, 01 Sep 2023 00:50:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:396b54ae4718b83d7c6883841d468209d8c79f5382b4148a5b3835b4b9b6b339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.0 KB (544980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1a1f7924a5378a723fae13cd15c54a88c86f0c768e17f27cd8976460290fa`

```dockerfile
```

-	Layers:
	-	`sha256:a797e5484c2dcf82e70da3013647e1a92d074c293f04e32b996f8660688fcb0b`  
		Last Modified: Fri, 01 Sep 2023 00:50:56 GMT  
		Size: 509.2 KB (509188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9d2d0c0999f0825ec9698e17f0d417a33969f31ecb068c065653be83dcabe2`  
		Last Modified: Fri, 01 Sep 2023 00:50:56 GMT  
		Size: 35.8 KB (35792 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6867a4e0d8ecb753be3ab97c6cc5bada77b6feb3551aca997e0908cf1fa0405c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52844239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376dbef29455e32b4f18a5a45b2beb6ee80715291d5fd615232ee849147fd7c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Wed, 30 Aug 2023 23:06:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENV DOCKER_VERSION=24.0.5
# Wed, 30 Aug 2023 23:06:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Wed, 30 Aug 2023 23:06:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.21.0
# Wed, 30 Aug 2023 23:06:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-x86_64'; 			sha256='08e549924823e97a3ea303c2309b812dfd5223b8be5ff96fe41bf75181ce0977'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv6'; 			sha256='058ec96bc81ddeb317d160a6dea5bd8ac65dc2e90afff86bcc31f3f818f3fc5a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv7'; 			sha256='d46dbbbf5723c45125277c7c75b757b22679962707b2276a6d52f35964583c42'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-aarch64'; 			sha256='5daf8d1a04cd649ad4a64221d0ca0cffcce33c740e60d5b15698545ce6d0436b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-ppc64le'; 			sha256='fadbb72890d72f1246b213c453ec90cf494f4f8ea3dda2f63678de53a7e97c15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-riscv64'; 			sha256='cd01536476864bd97c6ce3dfd317730535e51b2e252e9468de0379cc84298187'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-s390x'; 			sha256='dfa8ab3ccc83311a2a4fddc43654de06c13cadc7caf629a0ddeceabd24bb6308'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Aug 2023 23:06:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Aug 2023 23:06:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Aug 2023 23:06:33 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852f3ef0b5f9b77c7c21abf9035ed77c331514fd6aa1498370a5dbd3e2048b5`  
		Last Modified: Mon, 07 Aug 2023 22:18:57 GMT  
		Size: 2.0 MB (2024556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37278d121b4b21d7bddb02dabb1e78b7fc30c3f3a41e41d6f6967d040f3a1b54`  
		Last Modified: Mon, 07 Aug 2023 22:18:58 GMT  
		Size: 15.4 MB (15435452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c05b0ea06520d0d3c1e2b6753a684589ba3e17e586d4be8ad9ddfbb2d3b1d4c`  
		Last Modified: Mon, 07 Aug 2023 22:18:59 GMT  
		Size: 15.8 MB (15768051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4befa581740e7c16bd32ac4084ff4c844bf2f0b6d98a960ae6d432749bf00734`  
		Last Modified: Fri, 01 Sep 2023 01:23:07 GMT  
		Size: 16.3 MB (16283699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b1302e6182b6780648863bfc0936d688ac0026408b2a8741d9eb4e5622860`  
		Last Modified: Fri, 01 Sep 2023 01:23:06 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf66d53f7de3b4c8526595dd272c84645feecb105970dce4af187d82a3486b6`  
		Last Modified: Fri, 01 Sep 2023 01:23:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4968bdb89a604162d04d897daf1522e03c1577cefc976964927eb0d96c49f6`  
		Last Modified: Fri, 01 Sep 2023 01:23:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5c9a923156d15a19dd35f7252bb23092c7ae1855968ab56c0861c944a9ad664f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.9 KB (544863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea911433e88af9bc852d66a5b0d5b3efc8f5bcd700bf17f2b8ef155396cb2f2`

```dockerfile
```

-	Layers:
	-	`sha256:29f47faaab1183aa004102a8e610014463e8ee37e9708827a2133bb70b5f78b9`  
		Last Modified: Fri, 01 Sep 2023 01:23:06 GMT  
		Size: 509.2 KB (509224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751bae0b5fdd98a81bc06f2378cca2d129da32c92a3ffaeb3a60b12b72b7cc41`  
		Last Modified: Fri, 01 Sep 2023 01:23:06 GMT  
		Size: 35.6 KB (35639 bytes)  
		MIME: application/vnd.in-toto+json
