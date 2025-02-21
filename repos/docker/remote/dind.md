## `docker:dind`

```console
$ docker pull docker@sha256:e0b121dfc337c0f5a9703ef0914a392864bde6db811f2ba5bdd617a6e932073e
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

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:60d62f23a0201a2fe86efb90e0e4ded4d774cbcd2770c05042ae19b35edea9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140955844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1cc34984efd1c677e8fc11862dec7d1384b6332cd885feb6f5004cdb05f9f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-amd64'; 			sha256='90f154aff1b1b0010ca3e59f473a59a86b5fdf34ca1196829c622c4fbf5e92fe'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v6'; 			sha256='1a55ed189ee5c58b3d78459cf81d023a135a759c5ea3b7d1e2ad587cdfabac15'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v7'; 			sha256='542676a5aa32ecfcfcb27c56a0c8d91af42614ed5c0266e91ed0b55d90a15555'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm64'; 			sha256='5543113b559ca523726c8979defa24466e451dbfa6ffe42c278d22a3f76a327a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-ppc64le'; 			sha256='90c2748b59d0588cbd006e209ce8cecf202319213eba6542d01a5ce2f5c06f6e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-riscv64'; 			sha256='84148bbc57023004b186bf1ba618f987d9df51d3b588876bfc04f7a592fb9bc0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-s390x'; 			sha256='541b0fe136f003db4e0e5e4e3ec4ae00a647b50d398e7f63201d1ea712218132'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093ab420fbbffed20317774fa7f5606c81a35d5d210bcf798df87f95a9a669a6`  
		Last Modified: Thu, 20 Feb 2025 23:28:25 GMT  
		Size: 8.1 MB (8062979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2075bd5a9647812379253b406e9b8223b89c97b3b000789b2189da6386acd23`  
		Last Modified: Thu, 20 Feb 2025 23:28:13 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06cbe23efe061313b261d836fe09968cba15c060ebecf5d1b4d0bfa2387c65e`  
		Last Modified: Thu, 20 Feb 2025 23:28:28 GMT  
		Size: 19.5 MB (19492207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50a195575b1f8f6a2d38ffd0f29835297af70baa7b60f3da4979dde6695a5b5`  
		Last Modified: Thu, 20 Feb 2025 23:28:17 GMT  
		Size: 21.8 MB (21829528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51823643726d36145e83493463c55db34871e5d7aeae596a1aac7b3299c1109`  
		Last Modified: Thu, 20 Feb 2025 23:28:28 GMT  
		Size: 20.9 MB (20907759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca1e4b73fb3339ac07e5f110fdae5d876fae02bfca0784029f85514390ad2dc`  
		Last Modified: Thu, 20 Feb 2025 23:28:14 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a739d571117dbe6482f0c1d3c2b4fccb6db62328249abf235f739642cbc75cdb`  
		Last Modified: Thu, 20 Feb 2025 23:28:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3c996427363b010abddaf37e87298192dacf653f3dac7de48e1da37303bc3b`  
		Last Modified: Thu, 20 Feb 2025 23:28:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4de3b08d25ca2f9e2ac64eca4d52a764081621b0eeb020676d6da78af56145`  
		Last Modified: Fri, 21 Feb 2025 00:27:49 GMT  
		Size: 6.7 MB (6733027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39253269ba5ebd72c1a0450ebc78c14c5e7eabe8e40220b1aceb967692f088ae`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 90.3 KB (90319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14d8fc628e07886c8c95bf53a60dc1c498ce750d17bca11e1487143f81029e7`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6c36376d9b8232ab265a6948a59dffbe6c471d4bdf8357680abbc722bfac7b`  
		Last Modified: Fri, 21 Feb 2025 00:27:59 GMT  
		Size: 60.2 MB (60189729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce99a40015e6c0950ea719520a80dd6b2c976ece219243e0df17a2428742191`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5c0c0d8b303dda2b4f191bee455efc1e1fe5e13070cb4eb065345b44ec064a`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4715db4b639d32a55e58adbdffa462182eba87c9b8c1342f3adf71fe194195d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84177099806493cd1864708deb5f615c9dadd4843771c8b120b2e78919efb69`

```dockerfile
```

-	Layers:
	-	`sha256:fe91a1cef5303463be3669de421b6fad574f60240f570fea5de7ef4071c63c3b`  
		Last Modified: Fri, 21 Feb 2025 03:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:c7cabb4c9446674f961af9a2ed4dd1f33db806d5ad3ca75993d83310389db808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131619371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a8bd6b7bcddddf3f17d398ee3a17570fb76546e339625da07169afe8e1058c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-amd64'; 			sha256='90f154aff1b1b0010ca3e59f473a59a86b5fdf34ca1196829c622c4fbf5e92fe'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v6'; 			sha256='1a55ed189ee5c58b3d78459cf81d023a135a759c5ea3b7d1e2ad587cdfabac15'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v7'; 			sha256='542676a5aa32ecfcfcb27c56a0c8d91af42614ed5c0266e91ed0b55d90a15555'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm64'; 			sha256='5543113b559ca523726c8979defa24466e451dbfa6ffe42c278d22a3f76a327a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-ppc64le'; 			sha256='90c2748b59d0588cbd006e209ce8cecf202319213eba6542d01a5ce2f5c06f6e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-riscv64'; 			sha256='84148bbc57023004b186bf1ba618f987d9df51d3b588876bfc04f7a592fb9bc0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-s390x'; 			sha256='541b0fe136f003db4e0e5e4e3ec4ae00a647b50d398e7f63201d1ea712218132'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 21:07:35 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 21:07:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:30 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4549743bfb504f7c2e1261d60115ed066aac8d6da42bb6103aa3958d332c2f`  
		Last Modified: Thu, 20 Feb 2025 23:28:31 GMT  
		Size: 20.4 MB (20431960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8147a84c6998e72ef6346a3f2728fd9efa2ef2f1f158b043ecbca9ee2452c3ca`  
		Last Modified: Thu, 20 Feb 2025 23:28:20 GMT  
		Size: 19.7 MB (19668791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463b9473dd9348ce5332a8a0cfde550fe2f973472ab3780c0f5129be5ab0466`  
		Last Modified: Thu, 20 Feb 2025 23:28:17 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ae5bdd3e74c5caffe44e1c1673432a314bbfb26ddb5d726853aae8466c1b3d`  
		Last Modified: Thu, 20 Feb 2025 23:28:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecec829634f3ab7aec45d03f973738d825f19bcf25093a58e57b53b32868ca9a`  
		Last Modified: Thu, 20 Feb 2025 23:28:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ecffa9cb4f7ab9a88ae8770370dba6b487f75bf08a90eb0c7bfc3b981d1a31`  
		Last Modified: Fri, 21 Feb 2025 00:27:22 GMT  
		Size: 7.0 MB (7036897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb446eba910f43a28adb87d5ced01dcecbfd9b006cedbc6036e1d396b3b14f91`  
		Last Modified: Fri, 21 Feb 2025 00:27:13 GMT  
		Size: 89.9 KB (89856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc086985e70e2d9463967c88db3e96c9b4d0ad5e891ef80e76a5e0def8d68357`  
		Last Modified: Fri, 21 Feb 2025 00:27:12 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c3f2592750ac377ac54af21e6341bcdf5ee0fb58f1a85cbeab82a685f0a96f`  
		Last Modified: Fri, 21 Feb 2025 00:27:30 GMT  
		Size: 55.6 MB (55587083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0bbd086821f71aea0bef7416fb17e2102f1e121e157885686089dd372ebce4`  
		Last Modified: Fri, 21 Feb 2025 00:27:12 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80523ffd4baa3413dd4487168e941936bb361214f29528afb19886f1406d6d41`  
		Last Modified: Fri, 21 Feb 2025 00:27:11 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e9a88fd37cbcbf4e281c5ac4143f430bf2c440daf450f4d5202c9dea905b4d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3deeae8e7ac29b12f4b362354877560d3196024e8510410b2dd44425972fbdc1`

```dockerfile
```

-	Layers:
	-	`sha256:e561372ec8582fe387926bed63dac45f925b381059e2293bdd6a33ccc23e1299`  
		Last Modified: Fri, 21 Feb 2025 03:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f6fa57a14683e55f528a676c40e9c85777a12ca861930817995945841179f14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129956466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6368bca67e000b69fcd59d9891b4e9c0cb73abbcd824251bd4d1cd2339462c95`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-amd64'; 			sha256='90f154aff1b1b0010ca3e59f473a59a86b5fdf34ca1196829c622c4fbf5e92fe'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v6'; 			sha256='1a55ed189ee5c58b3d78459cf81d023a135a759c5ea3b7d1e2ad587cdfabac15'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v7'; 			sha256='542676a5aa32ecfcfcb27c56a0c8d91af42614ed5c0266e91ed0b55d90a15555'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm64'; 			sha256='5543113b559ca523726c8979defa24466e451dbfa6ffe42c278d22a3f76a327a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-ppc64le'; 			sha256='90c2748b59d0588cbd006e209ce8cecf202319213eba6542d01a5ce2f5c06f6e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-riscv64'; 			sha256='84148bbc57023004b186bf1ba618f987d9df51d3b588876bfc04f7a592fb9bc0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-s390x'; 			sha256='541b0fe136f003db4e0e5e4e3ec4ae00a647b50d398e7f63201d1ea712218132'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f53c313861c48344d9e9226887c4c5dc20c4118c1394a1dbd157537e402718a`  
		Last Modified: Thu, 20 Feb 2025 23:28:37 GMT  
		Size: 7.3 MB (7299507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf33a2a302f3d2a707aff0d5d68f91c597a714a9404ad032fe931bf88410d78`  
		Last Modified: Thu, 20 Feb 2025 23:28:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a0a793080656d5c501f771202a444ab3a466aebd11e641d466b472bf58d80`  
		Last Modified: Thu, 20 Feb 2025 23:28:30 GMT  
		Size: 17.4 MB (17444439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb2e8f749d019625171560d4093cb8e6a41818397db22104e4b58df85c02ccb`  
		Last Modified: Thu, 20 Feb 2025 23:28:41 GMT  
		Size: 20.4 MB (20411494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9445df66768a492974193bf02894f86148368b949b45247b72a852b216db00bd`  
		Last Modified: Thu, 20 Feb 2025 23:28:42 GMT  
		Size: 19.7 MB (19655144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3d3e3e438e1d5bcac2b8bfc6a6a8d99a8a4af3f3c7db09ea92eb443710f5e7`  
		Last Modified: Thu, 20 Feb 2025 23:28:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c11f908d731f5f69ccbdd612dcbab77bd20a032990471a53c2c91c0ccc46915`  
		Last Modified: Thu, 20 Feb 2025 23:28:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55edd4ae172c42bf200441ef1592dcdbaef416fc4c24c02c7bf2c632024095b2`  
		Last Modified: Thu, 20 Feb 2025 23:28:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52944e98f0ac85e66216159d279ac8fac61a5de6a6f02822e48c19a3fe24e3af`  
		Last Modified: Fri, 21 Feb 2025 00:27:47 GMT  
		Size: 6.4 MB (6366256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895ab7f297689a2d2255e257a12c6053d7280569dca0657e467c5cc3ff79855c`  
		Last Modified: Fri, 21 Feb 2025 00:27:38 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bb75bd4b472be18a14a8424698b86d32847c96d6af5354df1ec1cbff150f4`  
		Last Modified: Fri, 21 Feb 2025 00:27:38 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01336398cba41913bef4dbafe5c18fefabc39e7cf7956f824527956d42d56b`  
		Last Modified: Fri, 21 Feb 2025 00:27:57 GMT  
		Size: 55.6 MB (55587098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5027555c836d8fb99287c8867c3a65e04ebdb609b9741139133ca131d1f208`  
		Last Modified: Fri, 21 Feb 2025 00:27:38 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b055cfda5614d97c0847dab7a9232fb43012ed0aa3dd77b3aa1b8eadbf35113`  
		Last Modified: Fri, 21 Feb 2025 00:27:40 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b8596ad20ceb03294a77ef92a8655e7eacb98568dfaa61cf6e23a594b4aee42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632ea6d736f32f3cc1aabe7cabb1c3c2d1cf7e3f0fd2e96a8093440d5bb54827`

```dockerfile
```

-	Layers:
	-	`sha256:16e7af9cff122dae42b0b0c893268a92d5b85823299b1f31c59d259428a8c590`  
		Last Modified: Fri, 21 Feb 2025 03:07:33 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:977cb36f040bf3590122ea348b7dc903c9835161e6eef4cb24a0d64f0f196a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132351646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d722bce39016a5e27c5110c482858c43096cd5054df599a20cb631c6b6f3f378`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-amd64'; 			sha256='90f154aff1b1b0010ca3e59f473a59a86b5fdf34ca1196829c622c4fbf5e92fe'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v6'; 			sha256='1a55ed189ee5c58b3d78459cf81d023a135a759c5ea3b7d1e2ad587cdfabac15'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v7'; 			sha256='542676a5aa32ecfcfcb27c56a0c8d91af42614ed5c0266e91ed0b55d90a15555'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm64'; 			sha256='5543113b559ca523726c8979defa24466e451dbfa6ffe42c278d22a3f76a327a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-ppc64le'; 			sha256='90c2748b59d0588cbd006e209ce8cecf202319213eba6542d01a5ce2f5c06f6e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-riscv64'; 			sha256='84148bbc57023004b186bf1ba618f987d9df51d3b588876bfc04f7a592fb9bc0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-s390x'; 			sha256='541b0fe136f003db4e0e5e4e3ec4ae00a647b50d398e7f63201d1ea712218132'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1b527e08b4ec0bd858f270bd1c73b4eb69fa1f9681172710944f5fb1108ab6`  
		Last Modified: Thu, 20 Feb 2025 23:28:05 GMT  
		Size: 8.1 MB (8076421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6666d4412f9e63506ae44900e1fd00275b8dd56bbe117245f21edb533c07d9e`  
		Last Modified: Thu, 20 Feb 2025 23:27:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4c9136fffa5cbeb2e6117e4694c7ea906da81198a0531aaa32145decb90eae`  
		Last Modified: Thu, 20 Feb 2025 23:27:58 GMT  
		Size: 18.4 MB (18412787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23097b21275c4fb3c71e52f2e5c3c8f7067a8cbf5b0c1b039f0ce0a91d9d59b`  
		Last Modified: Thu, 20 Feb 2025 23:28:08 GMT  
		Size: 20.0 MB (20041329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d721ea2bff14447ba40479b5a9a89bec640f22c89c1fc9c19aa7a47574de36b`  
		Last Modified: Thu, 20 Feb 2025 23:28:08 GMT  
		Size: 19.2 MB (19175074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41991d98c29dcb0ec17305e50c51cf373a30b30101d0b83a7f42b78241bb9c9b`  
		Last Modified: Thu, 20 Feb 2025 23:27:54 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a048cb704bc6ffec227160a3c0f3b515e4d6a47cf5e32800aaf51921f0b8e3`  
		Last Modified: Thu, 20 Feb 2025 23:27:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76a992e94298f7dd06fb20218693c8af98bfeb787e13e641be48f54748de30`  
		Last Modified: Thu, 20 Feb 2025 23:27:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af98a0761b2250294aa8e0549f273a686b0d36d5a844d569ebd214391efc4d`  
		Last Modified: Fri, 21 Feb 2025 00:27:13 GMT  
		Size: 7.0 MB (6978823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d34ed087c6d3c67acd0789cf0a9067aa7a58b8c74b093d947c2a7aa9afc2257`  
		Last Modified: Fri, 21 Feb 2025 00:27:05 GMT  
		Size: 99.4 KB (99377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adb48987cb089b5c8e32479e1e556c0ea705b5350c8181f4c3e9258d93495d3`  
		Last Modified: Fri, 21 Feb 2025 00:27:04 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee8a14e1dc617c334a84e008c5304323aeb97ec7a165786b83a8cc30e3a9249`  
		Last Modified: Fri, 21 Feb 2025 00:27:22 GMT  
		Size: 55.6 MB (55566754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b655aeae01097cc967e1dcbc3277f9e2b29baddcbfed6e2018f83418c89b6530`  
		Last Modified: Fri, 21 Feb 2025 00:27:05 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143188afd15270b0b4487b8c02ad0ba5b50b863f02d99e3c41bb43df846c157a`  
		Last Modified: Fri, 21 Feb 2025 00:27:05 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:76dff41b9c863573e5b7913f235025acf4f98fb96f952dd24b5baad6189240c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f789cdd9f9dac243cb6496e4bac83c1a011329dc458db45a1e6e5c43951fb28`

```dockerfile
```

-	Layers:
	-	`sha256:9d9b26cdb189f2d40e5dfcdabc6def7dcbd157e33814f905fa4acee30b3c7653`  
		Last Modified: Fri, 21 Feb 2025 03:07:34 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json
