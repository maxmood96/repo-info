## `docker:24-dind`

```console
$ docker pull docker@sha256:c90e58d30700470fc59bdaaf802340fd25c1db628756d7bf74e100c566ba9589
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind` - linux; amd64

```console
$ docker pull docker@sha256:4c92bd9328191f76e8eec6592ceb2e248aa7406dfc9505870812cf8ebee9326a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118323616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa93deb4ad1b0d89a24411a139b6867bd175cfc69e0e8e087bfc69911f99943d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 23 Nov 2023 12:04:14 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["sh"]
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
VOLUME [/var/lib/docker]
# Tue, 28 Nov 2023 00:04:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 28 Nov 2023 00:04:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 28 Nov 2023 00:04:30 GMT
CMD []
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b285db406411a1695ce33eb622e3e6a6a7d53ab67c39f50c8e02a19d0b38cd1`  
		Last Modified: Fri, 01 Dec 2023 00:10:44 GMT  
		Size: 2.0 MB (2014283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d69b82b2d9a89b29e203c64413ad0f9710c51a85d6a2d43d36ec94344f36c6`  
		Last Modified: Fri, 01 Dec 2023 00:10:45 GMT  
		Size: 16.4 MB (16400379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6263b44eccfd4448ad0ccd1dbbb6f60488de19c1197312eb4bf936b1c74850`  
		Last Modified: Fri, 01 Dec 2023 00:10:45 GMT  
		Size: 17.2 MB (17195289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b160c2372a2b232aea5c7524bc21cb4bb4f71359c65ef2d148f1d87ff90e5a`  
		Last Modified: Fri, 01 Dec 2023 00:10:45 GMT  
		Size: 17.9 MB (17852056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512ee51c1482f78a905bb3b76bbdd6c07351726bdfff193f7bdc3133493c9b23`  
		Last Modified: Fri, 01 Dec 2023 00:10:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc5cfa8df57583c1b62f43b1e29f2ab4ff0a069945a6af8f1a61c4510b6677a`  
		Last Modified: Fri, 01 Dec 2023 00:10:47 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4552482a93ed5dcebc852515c3f25ba5a67e4c490dc154e2aa842a0ff96088`  
		Last Modified: Fri, 01 Dec 2023 00:10:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2a69f00e6a211d1b349b4e8cc0a3bc730b4d2205d2614f7e5b92fd9c75111a`  
		Last Modified: Fri, 01 Dec 2023 01:11:42 GMT  
		Size: 7.1 MB (7080230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61327588ac679078156678b73ec1552c5ec7739f9a023a468d7ea627c5d8e43`  
		Last Modified: Fri, 01 Dec 2023 01:11:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71ca9084160e32dbc8f0b03efa36774ecc4b283017670ff044436a00af869ce`  
		Last Modified: Fri, 01 Dec 2023 01:11:44 GMT  
		Size: 54.4 MB (54371654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3426bb08ce9019bdb767a52aae9761fdcf68536e5b45d10c16537f802015b0`  
		Last Modified: Fri, 01 Dec 2023 01:11:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96259b8b69c282f28fa8a7ac294761b02e534d6ba31716c22545a5c0e99de77`  
		Last Modified: Fri, 01 Dec 2023 01:11:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bd33f1033e5aa789410574b03beda7415cfc5b7826beba9148d9ca45395029a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 KB (706584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556f2ad73fca92c2d79ce79bde68fad94897ab79b2b995d9b5de5aa5ff88755d`

```dockerfile
```

-	Layers:
	-	`sha256:078c82be0aa93b09ab67b38f420d740d98edd25c6c98deabf84f9c553dcc0c03`  
		Last Modified: Fri, 01 Dec 2023 01:11:42 GMT  
		Size: 676.5 KB (676456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d934f70eac58ba572dada13786192a054e917792a9f37f88a8a2358cd1b3cc`  
		Last Modified: Fri, 01 Dec 2023 01:11:42 GMT  
		Size: 30.1 KB (30128 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:db900d48c4071b64779ab61dbc65f20a01dfc9955eec6013c575c6df2c178f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111480870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a54799b3fd63705a07b1c18be1f58a7ef8be02993bf506e0bfedf3e4f632c5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 23 Nov 2023 12:04:14 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["sh"]
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
VOLUME [/var/lib/docker]
# Tue, 28 Nov 2023 00:04:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 28 Nov 2023 00:04:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 28 Nov 2023 00:04:30 GMT
CMD []
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcbe62a68d12d326a6216794589666f3880a1b7f916f47a323045227af69af0`  
		Last Modified: Fri, 01 Dec 2023 11:44:39 GMT  
		Size: 2.1 MB (2088618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ad79711b20184b2218f91fb2627040d75679ad416c364743c641c4236878bb`  
		Last Modified: Fri, 01 Dec 2023 12:30:21 GMT  
		Size: 15.1 MB (15132562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6458f655a2af0d0627300ac79fe6ce10dd96c45dc9f237b4928f1b437d631f56`  
		Last Modified: Fri, 01 Dec 2023 12:30:20 GMT  
		Size: 16.1 MB (16099971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd022370c80f335f1d8c5d1fc54156ba5c902bf13096bbe129a1f8383357bafc`  
		Last Modified: Fri, 01 Dec 2023 12:30:20 GMT  
		Size: 16.9 MB (16867500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fac6b23d2a54bbef94347ccd7a70978901eb673c29eac57a897b636222a55bd`  
		Last Modified: Fri, 01 Dec 2023 12:30:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7ffb148d51f9100e26cc4dbb483c165e18ca40c30430b46a04055185a9b17f`  
		Last Modified: Fri, 01 Dec 2023 12:30:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1268a56cafc43bfb8c55f2f852ab980611ec33e44b383f48f88f2ee5d2b56298`  
		Last Modified: Fri, 01 Dec 2023 12:30:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cfbc448475d01176205df6eb378015eb29ebcf171f4a5517dac8195bfc4cb8`  
		Last Modified: Fri, 01 Dec 2023 13:25:42 GMT  
		Size: 7.2 MB (7173665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f59fc14e6c3178942df33b55aa9408b42e1dff4b422ad1bc730effa9580bdf7`  
		Last Modified: Fri, 01 Dec 2023 13:25:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4a608bb9382952fdb9905b05204228f43f310aefcc6a720685ff8c4087faab`  
		Last Modified: Fri, 01 Dec 2023 13:25:50 GMT  
		Size: 51.0 MB (50964377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c77e181750f8fb2fe91ac96a366b4efa0c838d5ef5dade590a4ab6e2ee8cf`  
		Last Modified: Fri, 01 Dec 2023 13:25:41 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4605a0ab65ba0190e16799ebccf8b2650fa67381c60fd0a3992523a799d18acd`  
		Last Modified: Fri, 01 Dec 2023 13:25:41 GMT  
		Size: 2.8 KB (2793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:dff21d22d9a1e8a1d927234ae319bbeb724737a921dc1a843fd218012b96e993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110281767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b968b536548c4ffec3d91a667d9ed7d7882e26c71d616fffeef7dc851dbc0e6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 23 Nov 2023 12:04:14 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["sh"]
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
VOLUME [/var/lib/docker]
# Tue, 28 Nov 2023 00:04:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 28 Nov 2023 00:04:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 28 Nov 2023 00:04:30 GMT
CMD []
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95efc36d5bd6e6f6cacfcd0475b060ca3cf0b73388d577a29cf0e1260082d17`  
		Last Modified: Fri, 01 Dec 2023 10:04:32 GMT  
		Size: 1.9 MB (1875249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97bf8a10fa37739e7b3eee3a033bd802e8685fc5d5e45367198561afd4a3d67`  
		Last Modified: Fri, 01 Dec 2023 10:32:11 GMT  
		Size: 15.1 MB (15127048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37834e511b4b47c828b1509580a35bc213a6fe6dd4d832e65097cabd22fb00dc`  
		Last Modified: Fri, 01 Dec 2023 10:32:11 GMT  
		Size: 16.1 MB (16084088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc3d3b7fdf893986e88bc2b64ab9033ce913f1dcc76b3a4574af9a5c8b7768a`  
		Last Modified: Fri, 01 Dec 2023 10:32:11 GMT  
		Size: 16.9 MB (16852960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ff49e012900825ffcc282c4fcb232c801b4f3c976fe38728c61c7068c2025a`  
		Last Modified: Fri, 01 Dec 2023 10:32:11 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699d5637291d52ed032e72bf8764080e3c6f271dbd73ee5e9b5e7e237facf74`  
		Last Modified: Fri, 01 Dec 2023 10:32:12 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b23b5726107c16767fe0596771eabbe3b3cefcfa427224580f4a35e384f05da`  
		Last Modified: Fri, 01 Dec 2023 10:32:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fe2666bc8ccee1118e120cdc30a8991e8600694adde7302d127641c91fdd3`  
		Last Modified: Fri, 01 Dec 2023 11:57:38 GMT  
		Size: 6.5 MB (6469751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7255f35ecd3ad68cfc350c8f283c2ebb8cdb61ad06c460725e597a1c69c88d5f`  
		Last Modified: Fri, 01 Dec 2023 11:57:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739ac8cf776ada89156969851bcde8489c20861bbc08724c394ef985687ce1b2`  
		Last Modified: Fri, 01 Dec 2023 11:57:39 GMT  
		Size: 51.0 MB (50964348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b4fc8b0c76303944c3dd09c60b427313273a514f7b3e54f8d216fe225f6331`  
		Last Modified: Fri, 01 Dec 2023 11:57:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21517b657ee56db16834a4c7ee3eea4f5c0ca0ca9b85513e7528631337d71232`  
		Last Modified: Fri, 01 Dec 2023 11:57:38 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9b19df42d31ff6d0bad19c17186093b153048b53ef33c7de0c9e76ae9a4412d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.9 KB (706873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a3c8802dbcb0e61664900c853917c022aa1bdc3cb2378a28d3b7dd432c5905`

```dockerfile
```

-	Layers:
	-	`sha256:f22a1505f0006dd306249a6016b56f84bbc715943fc8b4eac20a80e621f78fc3`  
		Last Modified: Fri, 01 Dec 2023 11:57:37 GMT  
		Size: 676.5 KB (676540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfacd2b7b9117914db45280f1c305cbeada460855c8da278f3b346464d95bc9a`  
		Last Modified: Fri, 01 Dec 2023 11:57:37 GMT  
		Size: 30.3 KB (30333 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2afeb0c1357ac43eb81976a3a84995645872ab18644f6799677cd786de54cf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109759921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df02599b74fe9ab4363f6c0255b7e5a2d55f87616a5852f6420400eb4383ebfd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 23 Nov 2023 12:04:14 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["sh"]
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 28 Nov 2023 00:04:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Nov 2023 00:04:30 GMT
VOLUME [/var/lib/docker]
# Tue, 28 Nov 2023 00:04:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 28 Nov 2023 00:04:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 28 Nov 2023 00:04:30 GMT
CMD []
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26858e57ca6ca6c73ea7609b8f22c6a8f69a2e37b3e4147e8b5e125aeb518205`  
		Last Modified: Fri, 01 Dec 2023 11:42:31 GMT  
		Size: 2.0 MB (2024551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86458aa83f1a2aa3861b502435d3633f41d5c7da792b53987c370e37ad659a59`  
		Last Modified: Fri, 01 Dec 2023 12:09:03 GMT  
		Size: 15.4 MB (15449534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9b634a3a747adfb494780a1378ecb8818b4508d34f1439ccbc79fc01083295`  
		Last Modified: Fri, 01 Dec 2023 12:09:03 GMT  
		Size: 15.6 MB (15640602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6335e39f2a7f78909f1cb6d76ab12c201e43710ead4c734e3fb7c21e3ec796cd`  
		Last Modified: Fri, 01 Dec 2023 12:09:03 GMT  
		Size: 16.3 MB (16302309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcc71d2fb031cf9bcea1c9e426783f4ca7bc6a38d9d6b043a22fc0aab5f4fe4`  
		Last Modified: Fri, 01 Dec 2023 12:09:02 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89b1a3de40072fe92ef3a3ee360daf7d52c82c50625c29c51c2b0c7c1ae347d`  
		Last Modified: Fri, 01 Dec 2023 12:09:03 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308929de9fc1af5c306384b48ff4570912438d9ac77a9497f39cb81d3f625e28`  
		Last Modified: Fri, 01 Dec 2023 12:09:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb6787439051badf1eaedbe1a7e30ccd7bef46d6cc3eb40d5fda04090b50b98`  
		Last Modified: Fri, 01 Dec 2023 14:32:11 GMT  
		Size: 7.3 MB (7291361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312901b09ecd31d5a138ebb8712f41f4c3d0c282f6a1496e9566bcbcd5b3c0c0`  
		Last Modified: Fri, 01 Dec 2023 14:32:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0703c105fb96f7379c4b55b8a37d100256f35abc60955431bf7af88f9d637046`  
		Last Modified: Fri, 01 Dec 2023 14:32:13 GMT  
		Size: 49.7 MB (49711211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26863318aaf89c5c8901650bdb47eb9786533e4f7db03f20a079ecbc7b526a`  
		Last Modified: Fri, 01 Dec 2023 14:32:11 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb8d2ec655e20ffcb9bd81ca7af77ae8e45983995ea39b29a00f2fc02f06d56`  
		Last Modified: Fri, 01 Dec 2023 14:32:12 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:885deeb2bb863dbcf0b80bceb8b5be84de59c6132926911ed0d591fa8232935d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.7 KB (706677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1263747495fe0f78fc9ea56b1422d61e204bb994aafec4f9365ca557c25b17`

```dockerfile
```

-	Layers:
	-	`sha256:3b6b9b871b011360553675744af374f516cda332fec47bed0e0e3dbd6e040698`  
		Last Modified: Fri, 01 Dec 2023 14:32:10 GMT  
		Size: 676.5 KB (676479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883a2e0f28cac4251a2ed2d4ee36343b23c800b90de8ca5f8ab099a8b7e8b71b`  
		Last Modified: Fri, 01 Dec 2023 14:32:10 GMT  
		Size: 30.2 KB (30198 bytes)  
		MIME: application/vnd.in-toto+json
