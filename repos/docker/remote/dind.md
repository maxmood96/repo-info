## `docker:dind`

```console
$ docker pull docker@sha256:3c6e4dca7a63c9a32a4e00da40461ce067f255987ccc9721cf18ffa087bcd1ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:78e33a72a1df68d3b4341630a215626e79e45725e205f0355dc05df1b81ad68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118557115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7015f2c475d511a251955877c2862016a4042512ba625ed905e69202f87e1a21`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 24 Jul 2023 16:17:39 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 24 Jul 2023 16:17:39 GMT
CMD ["/bin/sh"]
# Mon, 24 Jul 2023 16:17:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DOCKER_VERSION=24.0.5
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.21.0
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-x86_64'; 			sha256='08e549924823e97a3ea303c2309b812dfd5223b8be5ff96fe41bf75181ce0977'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv6'; 			sha256='058ec96bc81ddeb317d160a6dea5bd8ac65dc2e90afff86bcc31f3f818f3fc5a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv7'; 			sha256='d46dbbbf5723c45125277c7c75b757b22679962707b2276a6d52f35964583c42'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-aarch64'; 			sha256='5daf8d1a04cd649ad4a64221d0ca0cffcce33c740e60d5b15698545ce6d0436b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-ppc64le'; 			sha256='fadbb72890d72f1246b213c453ec90cf494f4f8ea3dda2f63678de53a7e97c15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-riscv64'; 			sha256='cd01536476864bd97c6ce3dfd317730535e51b2e252e9468de0379cc84298187'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-s390x'; 			sha256='dfa8ab3ccc83311a2a4fddc43654de06c13cadc7caf629a0ddeceabd24bb6308'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 24 Jul 2023 16:17:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jul 2023 16:17:39 GMT
CMD ["sh"]
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
VOLUME [/var/lib/docker]
# Mon, 24 Jul 2023 16:17:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 24 Jul 2023 16:17:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 24 Jul 2023 16:17:39 GMT
CMD []
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
	-	`sha256:aabff4d636f814f9819ae37656bba46b3252c9ff0d0370aaf21c1215f59ebe9f`  
		Last Modified: Fri, 01 Sep 2023 01:51:01 GMT  
		Size: 7.1 MB (7080310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75ebc365546d935f8a58388c34faa054bb5aabb20d80366d97f5c8c2ab14972`  
		Last Modified: Fri, 01 Sep 2023 01:51:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b27304de7143b6ca4436c805c33f9bd691b751177958bc907d5aebe91c8bd`  
		Last Modified: Fri, 01 Sep 2023 01:51:03 GMT  
		Size: 54.4 MB (54377552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4b9734a564f97a28163b6f682e51485d82c5da5049e67fdc3bfdc17f178703`  
		Last Modified: Fri, 01 Sep 2023 01:51:00 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc79f9020c0e1016b1ad9f651c87ce068efb1031e49f80f63a14892f59a6f17`  
		Last Modified: Fri, 01 Sep 2023 01:51:01 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:20f0d7c1e0ae8d99ea5f3501bfdda377cbef396dbd2cd8cd3c7fcd7597ee53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **787.0 KB (786975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888e0f2341b28c595a15c556b7de2ef7b2193098083e90eb91c6b2ece4e62bec`

```dockerfile
```

-	Layers:
	-	`sha256:03a9e1145cddad6d8a9abd6d2286a33aeb8a425a56d89b267f34fa0ab3583d19`  
		Last Modified: Fri, 01 Sep 2023 01:51:00 GMT  
		Size: 756.8 KB (756837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab5af778a6b0c2b95e4a1d9822191969109fc98ecde4850f146a3316b98a606`  
		Last Modified: Fri, 01 Sep 2023 01:51:00 GMT  
		Size: 30.1 KB (30138 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:901dc6a38f98d1d06349951cdb3ca2e9ccd584800cd993df01c05cedf2843b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109859474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b564bb4cc4b98471f04d1e557a0ab96507f66c49cde4467b977093ec650c5f1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 24 Jul 2023 16:17:39 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 24 Jul 2023 16:17:39 GMT
CMD ["/bin/sh"]
# Mon, 24 Jul 2023 16:17:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DOCKER_VERSION=24.0.5
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.21.0
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-x86_64'; 			sha256='08e549924823e97a3ea303c2309b812dfd5223b8be5ff96fe41bf75181ce0977'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv6'; 			sha256='058ec96bc81ddeb317d160a6dea5bd8ac65dc2e90afff86bcc31f3f818f3fc5a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv7'; 			sha256='d46dbbbf5723c45125277c7c75b757b22679962707b2276a6d52f35964583c42'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-aarch64'; 			sha256='5daf8d1a04cd649ad4a64221d0ca0cffcce33c740e60d5b15698545ce6d0436b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-ppc64le'; 			sha256='fadbb72890d72f1246b213c453ec90cf494f4f8ea3dda2f63678de53a7e97c15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-riscv64'; 			sha256='cd01536476864bd97c6ce3dfd317730535e51b2e252e9468de0379cc84298187'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-s390x'; 			sha256='dfa8ab3ccc83311a2a4fddc43654de06c13cadc7caf629a0ddeceabd24bb6308'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 24 Jul 2023 16:17:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jul 2023 16:17:39 GMT
CMD ["sh"]
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Mon, 24 Jul 2023 16:17:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jul 2023 16:17:39 GMT
VOLUME [/var/lib/docker]
# Mon, 24 Jul 2023 16:17:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 24 Jul 2023 16:17:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 24 Jul 2023 16:17:39 GMT
CMD []
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
	-	`sha256:36b1c38ea0707fa5c2044f95cdf9c13bdac6fe32c09dd351bfed7b736660e929`  
		Last Modified: Fri, 01 Sep 2023 01:53:33 GMT  
		Size: 7.3 MB (7291226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e97e89203332a18b4257fd34a3391ba96940d2a8ee15b2a911989ad2ba5be6`  
		Last Modified: Fri, 01 Sep 2023 01:53:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167a7c4f8d8d35722c7a9ceae69bf71295cce21e754beb50f02db0682c415769`  
		Last Modified: Fri, 01 Sep 2023 01:53:35 GMT  
		Size: 49.7 MB (49718887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a0355ba5d9012607a678f687402ca9a1b7b8084b4e19a41e944d4080f3409a`  
		Last Modified: Fri, 01 Sep 2023 01:53:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd53f0d7f1834bd427ab641a8e012e4a1d9d252191a5fe17322dd1e1f9ece852`  
		Last Modified: Fri, 01 Sep 2023 01:53:33 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:77cc4a62cc1fb365e00a9a862478351523483c725343bef1b5b22f1771c43c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **787.3 KB (787263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8daf7609eefe181ab4e37963a8fa890fb51c1b9cc55d830dc3b342df02116e`

```dockerfile
```

-	Layers:
	-	`sha256:bb166e5b7fefafbf2b267ea78ffbc0f9f613d29a85403496612c8793e9042840`  
		Last Modified: Fri, 01 Sep 2023 01:53:32 GMT  
		Size: 757.1 KB (757056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60cc6727f24722478cbb7a66e7581f4809f0f34e65a4820502072281db4b9df`  
		Last Modified: Fri, 01 Sep 2023 01:53:32 GMT  
		Size: 30.2 KB (30207 bytes)  
		MIME: application/vnd.in-toto+json
