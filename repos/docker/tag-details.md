<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-1809`](#docker28-windowsservercore-1809)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.0`](#docker280)
-	[`docker:28.0-cli`](#docker280-cli)
-	[`docker:28.0-dind`](#docker280-dind)
-	[`docker:28.0-dind-rootless`](#docker280-dind-rootless)
-	[`docker:28.0-windowsservercore`](#docker280-windowsservercore)
-	[`docker:28.0-windowsservercore-1809`](#docker280-windowsservercore-1809)
-	[`docker:28.0-windowsservercore-ltsc2022`](#docker280-windowsservercore-ltsc2022)
-	[`docker:28.0-windowsservercore-ltsc2025`](#docker280-windowsservercore-ltsc2025)
-	[`docker:28.0.0`](#docker2800)
-	[`docker:28.0.0-alpine3.21`](#docker2800-alpine321)
-	[`docker:28.0.0-cli`](#docker2800-cli)
-	[`docker:28.0.0-cli-alpine3.21`](#docker2800-cli-alpine321)
-	[`docker:28.0.0-dind`](#docker2800-dind)
-	[`docker:28.0.0-dind-alpine3.21`](#docker2800-dind-alpine321)
-	[`docker:28.0.0-dind-rootless`](#docker2800-dind-rootless)
-	[`docker:28.0.0-windowsservercore`](#docker2800-windowsservercore)
-	[`docker:28.0.0-windowsservercore-1809`](#docker2800-windowsservercore-1809)
-	[`docker:28.0.0-windowsservercore-ltsc2022`](#docker2800-windowsservercore-ltsc2022)
-	[`docker:28.0.0-windowsservercore-ltsc2025`](#docker2800-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

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

### `docker:28` - linux; amd64

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm variant v6

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm variant v7

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm64 variant v8

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

### `docker:28` - unknown; unknown

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

## `docker:28-cli`

```console
$ docker pull docker@sha256:887a9786ad5566037eb9ee72b1c90a90846b385a857258dc06e1e3f6488e43f4
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

### `docker:28-cli` - linux; amd64

```console
$ docker pull docker@sha256:8cdf18b080fc7b11649280c97dd147c328ea3c82cd09e4e85f0e3e446276d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73936867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ae8bc797f1ebb6b0e032d633fdd9970ca8222fb82f7c5faf28f4d06dd66343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:56e48ba725a90e5447bbbf222ba3b57958dba989c7455400ae0107705fb2edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29702f2c3193de88b7cc798155359414b597aba6cc6e132b4dc6a390229ab5c3`

```dockerfile
```

-	Layers:
	-	`sha256:a0c0c3a81b00183cb3c2d9219542a9321fee1e435151e642f2020bb23037a5e6`  
		Last Modified: Fri, 21 Feb 2025 03:07:42 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:9210cb4fabe4c615183ca805315c7447cfcf89645d7185701451633a9a73abf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68899628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8224895e513dedc9188d6307c9f130dbda5dd94cbf242f25396798350aae5da6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:81cf2965d6ada5e0a87e3e0e5f8aa430e3926d2bac634ca0a11edbaddc4a6e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb96212dc183aff17523a7009a25396a418828fb426f4f7334ca03ff284cc95c`

```dockerfile
```

-	Layers:
	-	`sha256:ede5804b676a2080c79e2f198a3486858b4f9790b3c5b2f3621147fa40edb83e`  
		Last Modified: Fri, 21 Feb 2025 03:07:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:64c3fe7a413de80105071682ae30585431da991cba570aebe1c413afefd63a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67910864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd4097f50aa5e6ca8a005f4ab41aae0743d7ad12ad3c781ed02ccfc5dea7fef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a4622d9c3bec5213e74c5c712b54ae10950233a5e84acc17342dade4cd94f156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba8c3d45c41d43975bf5c1e600922ff8b5d9124c55ac772332087a4cd7bccd4`

```dockerfile
```

-	Layers:
	-	`sha256:8bb09b223df08d8d29f9dce0774ccbd2af9bddac2ad6d4ecc20ee8300d59cd18`  
		Last Modified: Fri, 21 Feb 2025 03:07:44 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dcf2e37500a110aed81793b6a22e21fc806cb1a97ff52ceacd8ac95d20f1363b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f8e9cc2b73b8198319ff8105b4487146527454e6585d3f9cdf92e47a1f6e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0954244e6afa38c31fcb4d785e11c0d073dc1cf43924942c190b998143e00ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd92ef9ae240d50c51adc27276ab23ab1085129b09a03978d52a758c813668c`

```dockerfile
```

-	Layers:
	-	`sha256:2e9175a11d2049bf2a2ba3456fb7de475c4b2595a4404f3a03ea0056a2e4677f`  
		Last Modified: Fri, 21 Feb 2025 03:07:45 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

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

### `docker:28-dind` - linux; amd64

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm variant v6

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm variant v7

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm64 variant v8

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

### `docker:28-dind` - unknown; unknown

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

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:c2bdebd237ff73eb4cd004c3d06b91266c8e71fc0eb50cc05b7141f48da9c09b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:baeccb921bfefe9c0abbaf4c27899cc82a1ae8ef8b0bb6647f15ff19a26f1edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159110162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28922b4b7da0159cbf39d0f3a53b9f370655bc0bbdc2253fba400c65b1089dbe`
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
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
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
	-	`sha256:3c751079331c0d7cc77480ccc642bc7a155d54c6407ca58d109a4778a1d219d2`  
		Last Modified: Fri, 21 Feb 2025 01:07:58 GMT  
		Size: 986.6 KB (986567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abccb6ae0375cfd973e871cf8d9498f1137b801e03a1247896fef51459e842b`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279c452f347f576f445fcf89a42c79cef749c5ebf56f8654cb408c36b72596d`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f130ec6bab014d4e4217287e6a9e8ab3c9654578a2d7b81bd9e802b5348cdab`  
		Last Modified: Fri, 21 Feb 2025 01:08:06 GMT  
		Size: 17.2 MB (17166410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6167de8683d8d2c2fcdd7ccb8ebdd22f6b74a4c0c5b83a37d19baaec3c03c`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9b955e2017dc28a3f65f19a930b1245d79fc50869bcf22fb8b9c913bb3651ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb37c52b27e1569e14a67a20fae6f966ceb6926a5abbc2caf93ddc13d67f3430`

```dockerfile
```

-	Layers:
	-	`sha256:6ead672c435cbfcda4dc2151539470781c44ee6fe14e6aeb54abde9de0a82dcc`  
		Last Modified: Fri, 21 Feb 2025 03:07:51 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f8c1cb5a95beb1d7b5b9b55eb239c8e6faf24d0165eefcf3f043e6ed79d64afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152646612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2b5c4ab8d0497964a390eff576c882a14316c7c91817e4f79a67643a89aff9`
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
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
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
	-	`sha256:9f29180dea49ae66c7bc7926ee0ccd3bef65d1fabf038525fa152b1bad745f06`  
		Last Modified: Fri, 21 Feb 2025 01:07:52 GMT  
		Size: 1.0 MB (1014193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc68779566c657f24c79525ad9dcd5c9ee3ffcf02ec3c46a5cda60769586c2f`  
		Last Modified: Fri, 21 Feb 2025 01:07:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc41d26c599adbd498428291a25daa08bec1d395f5041788675dc4b6d6e912ae`  
		Last Modified: Fri, 21 Feb 2025 01:07:47 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9644daeeb7cd964b27d9fb1da77a254ecb25c2c25b5af0ca854b2d116ce08`  
		Last Modified: Fri, 21 Feb 2025 01:08:01 GMT  
		Size: 19.3 MB (19279435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f32d46f74022d488c81b4699aacff888d0301c2604d5665e93a34637c0742c7`  
		Last Modified: Fri, 21 Feb 2025 01:07:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:678f2f3f2fb1f6f4f47993ee1e513d82b0bf087173fa5d5ea2959690983a29c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fcb6725765cad4c7473f3e074b75927da8619de4e33f364720a8516ba1ac21`

```dockerfile
```

-	Layers:
	-	`sha256:5fe70a257c51d2754ab1d2db0953e9c3dd069fc47ea471e1c648a72885f409b3`  
		Last Modified: Fri, 21 Feb 2025 03:07:52 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:42bea6bfadb1655060b67b4af39235b2befa0d07799d5348506e6b43682b0af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:35:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:35:57 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:8c87e235530294d2b88d865e9b73352d741bf135bb5d7996357cc1259e792013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328621027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8baca22cc4eb365396c38a0c864ca7ce92d7a6a9f746db6704272ddb0e3b282`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 20 Feb 2025 23:38:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:39:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:39:21 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:39:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:39:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fea355b62ca4572b994dc74c2715f6d0e572dee1dde122c1b9667ba29a52bc`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4add6994a30cf2372676e5f6dcc501322c314740cbbaa81aedfd7f34fd114`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 365.4 KB (365409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfeb2a4441074cfb72ba4bbfb54d10e780fed5ebd4282f5aabb1d10a001b29b`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f37810d123d73eb77f2e07547d933af7005c60006ef944be2dc10aef6324ed7`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3cd08c82763ba826aa7f7c8e2fb0f7d38ded99fa8ceeb30dd0ed7c9fd2e2cf`  
		Last Modified: Thu, 20 Feb 2025 23:41:05 GMT  
		Size: 19.8 MB (19808968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad43392a0fb22c04f2fa5cf91d4e11ec2a6c1ade3934b213ebf918efa33e68`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2b5ed6114086b1deb97a464286804f8378784b8a76534f433dd3af1e5e706`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bc64e43a7efc1920189c900466e96f283a332d8c1a3a72cd6faa9e058dc37f`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eea4a39141050304ffd8c8247b3cb3779dbe12b30c278321f2454c7880a504`  
		Last Modified: Thu, 20 Feb 2025 23:41:16 GMT  
		Size: 22.7 MB (22747811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4b9a6967d16d3acceb3fdb5931bc90756517ecfa050319e2ac963a3a103a1`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21b04e127078d780548cf476f502da6ea984f45478286b4442eec97295207a`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053a644814e3f4033758fd3178c1a08ec78ce6d25c0942cdf4e18465a756517`  
		Last Modified: Thu, 20 Feb 2025 23:41:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c4aa754555e50ae5def00c6bafb9a987221023c5e0f47dd1c064adf20dbf9`  
		Last Modified: Thu, 20 Feb 2025 23:41:17 GMT  
		Size: 21.8 MB (21829214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:50d0bfde03e0b6f40598d31e004c4bb2403a80c9fff9f3934f2cd9f4727dabe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201683757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41ca21d8b613f4b46e76253dc47469b785006575cbbfa3f3e710f82a7cefdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 20 Feb 2025 23:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:37:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:37:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:37:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:37:32 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:37:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7a1d363a7cbc76c8803b0b2bfe5892407eef1a2c8f2a703812077cca802fb`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68969c343b72ab00102b3454a5042bcddfe3b4e214ca6b9f25c1054157bf873f`  
		Last Modified: Thu, 20 Feb 2025 23:38:44 GMT  
		Size: 356.6 KB (356613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd531517a87fb70100fecd706d41d299866177bd6e79eaef5172574a94e5127f`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac190ca9022227c882e04edfe0565f94fc3ea450ed8ed03fcfc10cb7e3a78ed`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630d6ec4dd535487f3145d617fe15227b850ecebc3613240658f71f4cf41486`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 19.8 MB (19818182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2275ba90e41fea0e66b50f7e6e5c34e084b069ecdefa9a42a7841db475798`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22539d4654b28662e6c4e0bd90de707de4d9815125015add8119448b286ef`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ede31d628f2b1abb82df21bfe3df1b33777312763d138c5c6039a6836608bf`  
		Last Modified: Thu, 20 Feb 2025 23:38:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08e15c1d44c604540ec54984f8dc55dd1d8ce7b7f7022714e63aa0d4c657eb0`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 22.8 MB (22756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce614b28a9ab99b1233346d2807b68b6369e28e3dd2a09189393474c522c92a`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74939f5df35bb4dc1e17acd099963211f6438d8871b89c20864b13fe92c47`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c24f4a68afc8435ccb724cefc8d7c92e0411f2123301aa269ecce5ef8319ba`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2860f40f04ae4699daca17122267a4f8c37df8e61f22a5ef5552029d29feb`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 21.8 MB (21831256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:129835b071beea9e35dbec8b6c134b387ff94e9f28e7b92a74079c74cb2812d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:50d0bfde03e0b6f40598d31e004c4bb2403a80c9fff9f3934f2cd9f4727dabe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201683757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41ca21d8b613f4b46e76253dc47469b785006575cbbfa3f3e710f82a7cefdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 20 Feb 2025 23:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:37:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:37:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:37:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:37:32 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:37:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7a1d363a7cbc76c8803b0b2bfe5892407eef1a2c8f2a703812077cca802fb`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68969c343b72ab00102b3454a5042bcddfe3b4e214ca6b9f25c1054157bf873f`  
		Last Modified: Thu, 20 Feb 2025 23:38:44 GMT  
		Size: 356.6 KB (356613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd531517a87fb70100fecd706d41d299866177bd6e79eaef5172574a94e5127f`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac190ca9022227c882e04edfe0565f94fc3ea450ed8ed03fcfc10cb7e3a78ed`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630d6ec4dd535487f3145d617fe15227b850ecebc3613240658f71f4cf41486`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 19.8 MB (19818182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2275ba90e41fea0e66b50f7e6e5c34e084b069ecdefa9a42a7841db475798`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22539d4654b28662e6c4e0bd90de707de4d9815125015add8119448b286ef`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ede31d628f2b1abb82df21bfe3df1b33777312763d138c5c6039a6836608bf`  
		Last Modified: Thu, 20 Feb 2025 23:38:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08e15c1d44c604540ec54984f8dc55dd1d8ce7b7f7022714e63aa0d4c657eb0`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 22.8 MB (22756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce614b28a9ab99b1233346d2807b68b6369e28e3dd2a09189393474c522c92a`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74939f5df35bb4dc1e17acd099963211f6438d8871b89c20864b13fe92c47`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c24f4a68afc8435ccb724cefc8d7c92e0411f2123301aa269ecce5ef8319ba`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2860f40f04ae4699daca17122267a4f8c37df8e61f22a5ef5552029d29feb`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 21.8 MB (21831256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:63142c95c405e1018b42a36af9d368023e4db8ea8d9e9e45d7120f9340348705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:8c87e235530294d2b88d865e9b73352d741bf135bb5d7996357cc1259e792013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328621027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8baca22cc4eb365396c38a0c864ca7ce92d7a6a9f746db6704272ddb0e3b282`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 20 Feb 2025 23:38:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:39:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:39:21 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:39:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:39:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fea355b62ca4572b994dc74c2715f6d0e572dee1dde122c1b9667ba29a52bc`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4add6994a30cf2372676e5f6dcc501322c314740cbbaa81aedfd7f34fd114`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 365.4 KB (365409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfeb2a4441074cfb72ba4bbfb54d10e780fed5ebd4282f5aabb1d10a001b29b`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f37810d123d73eb77f2e07547d933af7005c60006ef944be2dc10aef6324ed7`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3cd08c82763ba826aa7f7c8e2fb0f7d38ded99fa8ceeb30dd0ed7c9fd2e2cf`  
		Last Modified: Thu, 20 Feb 2025 23:41:05 GMT  
		Size: 19.8 MB (19808968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad43392a0fb22c04f2fa5cf91d4e11ec2a6c1ade3934b213ebf918efa33e68`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2b5ed6114086b1deb97a464286804f8378784b8a76534f433dd3af1e5e706`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bc64e43a7efc1920189c900466e96f283a332d8c1a3a72cd6faa9e058dc37f`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eea4a39141050304ffd8c8247b3cb3779dbe12b30c278321f2454c7880a504`  
		Last Modified: Thu, 20 Feb 2025 23:41:16 GMT  
		Size: 22.7 MB (22747811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4b9a6967d16d3acceb3fdb5931bc90756517ecfa050319e2ac963a3a103a1`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21b04e127078d780548cf476f502da6ea984f45478286b4442eec97295207a`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053a644814e3f4033758fd3178c1a08ec78ce6d25c0942cdf4e18465a756517`  
		Last Modified: Thu, 20 Feb 2025 23:41:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c4aa754555e50ae5def00c6bafb9a987221023c5e0f47dd1c064adf20dbf9`  
		Last Modified: Thu, 20 Feb 2025 23:41:17 GMT  
		Size: 21.8 MB (21829214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d99acb3911040c398b54e203664f1bb3f30d631567e6c22f94471cd2a07bf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:35:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:35:57 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0`

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

### `docker:28.0` - linux; amd64

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

### `docker:28.0` - unknown; unknown

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

### `docker:28.0` - linux; arm variant v6

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

### `docker:28.0` - unknown; unknown

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

### `docker:28.0` - linux; arm variant v7

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

### `docker:28.0` - unknown; unknown

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

### `docker:28.0` - linux; arm64 variant v8

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

### `docker:28.0` - unknown; unknown

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

## `docker:28.0-cli`

```console
$ docker pull docker@sha256:887a9786ad5566037eb9ee72b1c90a90846b385a857258dc06e1e3f6488e43f4
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

### `docker:28.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:8cdf18b080fc7b11649280c97dd147c328ea3c82cd09e4e85f0e3e446276d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73936867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ae8bc797f1ebb6b0e032d633fdd9970ca8222fb82f7c5faf28f4d06dd66343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:56e48ba725a90e5447bbbf222ba3b57958dba989c7455400ae0107705fb2edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29702f2c3193de88b7cc798155359414b597aba6cc6e132b4dc6a390229ab5c3`

```dockerfile
```

-	Layers:
	-	`sha256:a0c0c3a81b00183cb3c2d9219542a9321fee1e435151e642f2020bb23037a5e6`  
		Last Modified: Fri, 21 Feb 2025 03:07:42 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:9210cb4fabe4c615183ca805315c7447cfcf89645d7185701451633a9a73abf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68899628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8224895e513dedc9188d6307c9f130dbda5dd94cbf242f25396798350aae5da6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:81cf2965d6ada5e0a87e3e0e5f8aa430e3926d2bac634ca0a11edbaddc4a6e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb96212dc183aff17523a7009a25396a418828fb426f4f7334ca03ff284cc95c`

```dockerfile
```

-	Layers:
	-	`sha256:ede5804b676a2080c79e2f198a3486858b4f9790b3c5b2f3621147fa40edb83e`  
		Last Modified: Fri, 21 Feb 2025 03:07:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:64c3fe7a413de80105071682ae30585431da991cba570aebe1c413afefd63a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67910864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd4097f50aa5e6ca8a005f4ab41aae0743d7ad12ad3c781ed02ccfc5dea7fef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a4622d9c3bec5213e74c5c712b54ae10950233a5e84acc17342dade4cd94f156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba8c3d45c41d43975bf5c1e600922ff8b5d9124c55ac772332087a4cd7bccd4`

```dockerfile
```

-	Layers:
	-	`sha256:8bb09b223df08d8d29f9dce0774ccbd2af9bddac2ad6d4ecc20ee8300d59cd18`  
		Last Modified: Fri, 21 Feb 2025 03:07:44 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dcf2e37500a110aed81793b6a22e21fc806cb1a97ff52ceacd8ac95d20f1363b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f8e9cc2b73b8198319ff8105b4487146527454e6585d3f9cdf92e47a1f6e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0954244e6afa38c31fcb4d785e11c0d073dc1cf43924942c190b998143e00ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd92ef9ae240d50c51adc27276ab23ab1085129b09a03978d52a758c813668c`

```dockerfile
```

-	Layers:
	-	`sha256:2e9175a11d2049bf2a2ba3456fb7de475c4b2595a4404f3a03ea0056a2e4677f`  
		Last Modified: Fri, 21 Feb 2025 03:07:45 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind`

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

### `docker:28.0-dind` - linux; amd64

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

### `docker:28.0-dind` - unknown; unknown

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

### `docker:28.0-dind` - linux; arm variant v6

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

### `docker:28.0-dind` - unknown; unknown

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

### `docker:28.0-dind` - linux; arm variant v7

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

### `docker:28.0-dind` - unknown; unknown

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

### `docker:28.0-dind` - linux; arm64 variant v8

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

### `docker:28.0-dind` - unknown; unknown

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

## `docker:28.0-dind-rootless`

```console
$ docker pull docker@sha256:c2bdebd237ff73eb4cd004c3d06b91266c8e71fc0eb50cc05b7141f48da9c09b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:baeccb921bfefe9c0abbaf4c27899cc82a1ae8ef8b0bb6647f15ff19a26f1edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159110162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28922b4b7da0159cbf39d0f3a53b9f370655bc0bbdc2253fba400c65b1089dbe`
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
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
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
	-	`sha256:3c751079331c0d7cc77480ccc642bc7a155d54c6407ca58d109a4778a1d219d2`  
		Last Modified: Fri, 21 Feb 2025 01:07:58 GMT  
		Size: 986.6 KB (986567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abccb6ae0375cfd973e871cf8d9498f1137b801e03a1247896fef51459e842b`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279c452f347f576f445fcf89a42c79cef749c5ebf56f8654cb408c36b72596d`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f130ec6bab014d4e4217287e6a9e8ab3c9654578a2d7b81bd9e802b5348cdab`  
		Last Modified: Fri, 21 Feb 2025 01:08:06 GMT  
		Size: 17.2 MB (17166410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6167de8683d8d2c2fcdd7ccb8ebdd22f6b74a4c0c5b83a37d19baaec3c03c`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9b955e2017dc28a3f65f19a930b1245d79fc50869bcf22fb8b9c913bb3651ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb37c52b27e1569e14a67a20fae6f966ceb6926a5abbc2caf93ddc13d67f3430`

```dockerfile
```

-	Layers:
	-	`sha256:6ead672c435cbfcda4dc2151539470781c44ee6fe14e6aeb54abde9de0a82dcc`  
		Last Modified: Fri, 21 Feb 2025 03:07:51 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f8c1cb5a95beb1d7b5b9b55eb239c8e6faf24d0165eefcf3f043e6ed79d64afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152646612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2b5c4ab8d0497964a390eff576c882a14316c7c91817e4f79a67643a89aff9`
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
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
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
	-	`sha256:9f29180dea49ae66c7bc7926ee0ccd3bef65d1fabf038525fa152b1bad745f06`  
		Last Modified: Fri, 21 Feb 2025 01:07:52 GMT  
		Size: 1.0 MB (1014193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc68779566c657f24c79525ad9dcd5c9ee3ffcf02ec3c46a5cda60769586c2f`  
		Last Modified: Fri, 21 Feb 2025 01:07:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc41d26c599adbd498428291a25daa08bec1d395f5041788675dc4b6d6e912ae`  
		Last Modified: Fri, 21 Feb 2025 01:07:47 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9644daeeb7cd964b27d9fb1da77a254ecb25c2c25b5af0ca854b2d116ce08`  
		Last Modified: Fri, 21 Feb 2025 01:08:01 GMT  
		Size: 19.3 MB (19279435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f32d46f74022d488c81b4699aacff888d0301c2604d5665e93a34637c0742c7`  
		Last Modified: Fri, 21 Feb 2025 01:07:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:678f2f3f2fb1f6f4f47993ee1e513d82b0bf087173fa5d5ea2959690983a29c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fcb6725765cad4c7473f3e074b75927da8619de4e33f364720a8516ba1ac21`

```dockerfile
```

-	Layers:
	-	`sha256:5fe70a257c51d2754ab1d2db0953e9c3dd069fc47ea471e1c648a72885f409b3`  
		Last Modified: Fri, 21 Feb 2025 03:07:52 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-windowsservercore`

```console
$ docker pull docker@sha256:42bea6bfadb1655060b67b4af39235b2befa0d07799d5348506e6b43682b0af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:28.0-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:35:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:35:57 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:8c87e235530294d2b88d865e9b73352d741bf135bb5d7996357cc1259e792013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328621027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8baca22cc4eb365396c38a0c864ca7ce92d7a6a9f746db6704272ddb0e3b282`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 20 Feb 2025 23:38:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:39:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:39:21 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:39:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:39:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fea355b62ca4572b994dc74c2715f6d0e572dee1dde122c1b9667ba29a52bc`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4add6994a30cf2372676e5f6dcc501322c314740cbbaa81aedfd7f34fd114`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 365.4 KB (365409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfeb2a4441074cfb72ba4bbfb54d10e780fed5ebd4282f5aabb1d10a001b29b`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f37810d123d73eb77f2e07547d933af7005c60006ef944be2dc10aef6324ed7`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3cd08c82763ba826aa7f7c8e2fb0f7d38ded99fa8ceeb30dd0ed7c9fd2e2cf`  
		Last Modified: Thu, 20 Feb 2025 23:41:05 GMT  
		Size: 19.8 MB (19808968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad43392a0fb22c04f2fa5cf91d4e11ec2a6c1ade3934b213ebf918efa33e68`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2b5ed6114086b1deb97a464286804f8378784b8a76534f433dd3af1e5e706`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bc64e43a7efc1920189c900466e96f283a332d8c1a3a72cd6faa9e058dc37f`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eea4a39141050304ffd8c8247b3cb3779dbe12b30c278321f2454c7880a504`  
		Last Modified: Thu, 20 Feb 2025 23:41:16 GMT  
		Size: 22.7 MB (22747811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4b9a6967d16d3acceb3fdb5931bc90756517ecfa050319e2ac963a3a103a1`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21b04e127078d780548cf476f502da6ea984f45478286b4442eec97295207a`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053a644814e3f4033758fd3178c1a08ec78ce6d25c0942cdf4e18465a756517`  
		Last Modified: Thu, 20 Feb 2025 23:41:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c4aa754555e50ae5def00c6bafb9a987221023c5e0f47dd1c064adf20dbf9`  
		Last Modified: Thu, 20 Feb 2025 23:41:17 GMT  
		Size: 21.8 MB (21829214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:50d0bfde03e0b6f40598d31e004c4bb2403a80c9fff9f3934f2cd9f4727dabe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201683757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41ca21d8b613f4b46e76253dc47469b785006575cbbfa3f3e710f82a7cefdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 20 Feb 2025 23:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:37:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:37:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:37:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:37:32 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:37:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7a1d363a7cbc76c8803b0b2bfe5892407eef1a2c8f2a703812077cca802fb`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68969c343b72ab00102b3454a5042bcddfe3b4e214ca6b9f25c1054157bf873f`  
		Last Modified: Thu, 20 Feb 2025 23:38:44 GMT  
		Size: 356.6 KB (356613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd531517a87fb70100fecd706d41d299866177bd6e79eaef5172574a94e5127f`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac190ca9022227c882e04edfe0565f94fc3ea450ed8ed03fcfc10cb7e3a78ed`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630d6ec4dd535487f3145d617fe15227b850ecebc3613240658f71f4cf41486`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 19.8 MB (19818182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2275ba90e41fea0e66b50f7e6e5c34e084b069ecdefa9a42a7841db475798`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22539d4654b28662e6c4e0bd90de707de4d9815125015add8119448b286ef`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ede31d628f2b1abb82df21bfe3df1b33777312763d138c5c6039a6836608bf`  
		Last Modified: Thu, 20 Feb 2025 23:38:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08e15c1d44c604540ec54984f8dc55dd1d8ce7b7f7022714e63aa0d4c657eb0`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 22.8 MB (22756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce614b28a9ab99b1233346d2807b68b6369e28e3dd2a09189393474c522c92a`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74939f5df35bb4dc1e17acd099963211f6438d8871b89c20864b13fe92c47`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c24f4a68afc8435ccb724cefc8d7c92e0411f2123301aa269ecce5ef8319ba`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2860f40f04ae4699daca17122267a4f8c37df8e61f22a5ef5552029d29feb`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 21.8 MB (21831256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:129835b071beea9e35dbec8b6c134b387ff94e9f28e7b92a74079c74cb2812d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:28.0-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:50d0bfde03e0b6f40598d31e004c4bb2403a80c9fff9f3934f2cd9f4727dabe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201683757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41ca21d8b613f4b46e76253dc47469b785006575cbbfa3f3e710f82a7cefdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 20 Feb 2025 23:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:37:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:37:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:37:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:37:32 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:37:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7a1d363a7cbc76c8803b0b2bfe5892407eef1a2c8f2a703812077cca802fb`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68969c343b72ab00102b3454a5042bcddfe3b4e214ca6b9f25c1054157bf873f`  
		Last Modified: Thu, 20 Feb 2025 23:38:44 GMT  
		Size: 356.6 KB (356613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd531517a87fb70100fecd706d41d299866177bd6e79eaef5172574a94e5127f`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac190ca9022227c882e04edfe0565f94fc3ea450ed8ed03fcfc10cb7e3a78ed`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630d6ec4dd535487f3145d617fe15227b850ecebc3613240658f71f4cf41486`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 19.8 MB (19818182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2275ba90e41fea0e66b50f7e6e5c34e084b069ecdefa9a42a7841db475798`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22539d4654b28662e6c4e0bd90de707de4d9815125015add8119448b286ef`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ede31d628f2b1abb82df21bfe3df1b33777312763d138c5c6039a6836608bf`  
		Last Modified: Thu, 20 Feb 2025 23:38:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08e15c1d44c604540ec54984f8dc55dd1d8ce7b7f7022714e63aa0d4c657eb0`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 22.8 MB (22756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce614b28a9ab99b1233346d2807b68b6369e28e3dd2a09189393474c522c92a`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74939f5df35bb4dc1e17acd099963211f6438d8871b89c20864b13fe92c47`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c24f4a68afc8435ccb724cefc8d7c92e0411f2123301aa269ecce5ef8319ba`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2860f40f04ae4699daca17122267a4f8c37df8e61f22a5ef5552029d29feb`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 21.8 MB (21831256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:63142c95c405e1018b42a36af9d368023e4db8ea8d9e9e45d7120f9340348705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:28.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:8c87e235530294d2b88d865e9b73352d741bf135bb5d7996357cc1259e792013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328621027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8baca22cc4eb365396c38a0c864ca7ce92d7a6a9f746db6704272ddb0e3b282`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 20 Feb 2025 23:38:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:39:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:39:21 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:39:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:39:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fea355b62ca4572b994dc74c2715f6d0e572dee1dde122c1b9667ba29a52bc`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4add6994a30cf2372676e5f6dcc501322c314740cbbaa81aedfd7f34fd114`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 365.4 KB (365409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfeb2a4441074cfb72ba4bbfb54d10e780fed5ebd4282f5aabb1d10a001b29b`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f37810d123d73eb77f2e07547d933af7005c60006ef944be2dc10aef6324ed7`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3cd08c82763ba826aa7f7c8e2fb0f7d38ded99fa8ceeb30dd0ed7c9fd2e2cf`  
		Last Modified: Thu, 20 Feb 2025 23:41:05 GMT  
		Size: 19.8 MB (19808968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad43392a0fb22c04f2fa5cf91d4e11ec2a6c1ade3934b213ebf918efa33e68`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2b5ed6114086b1deb97a464286804f8378784b8a76534f433dd3af1e5e706`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bc64e43a7efc1920189c900466e96f283a332d8c1a3a72cd6faa9e058dc37f`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eea4a39141050304ffd8c8247b3cb3779dbe12b30c278321f2454c7880a504`  
		Last Modified: Thu, 20 Feb 2025 23:41:16 GMT  
		Size: 22.7 MB (22747811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4b9a6967d16d3acceb3fdb5931bc90756517ecfa050319e2ac963a3a103a1`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21b04e127078d780548cf476f502da6ea984f45478286b4442eec97295207a`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053a644814e3f4033758fd3178c1a08ec78ce6d25c0942cdf4e18465a756517`  
		Last Modified: Thu, 20 Feb 2025 23:41:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c4aa754555e50ae5def00c6bafb9a987221023c5e0f47dd1c064adf20dbf9`  
		Last Modified: Thu, 20 Feb 2025 23:41:17 GMT  
		Size: 21.8 MB (21829214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d99acb3911040c398b54e203664f1bb3f30d631567e6c22f94471cd2a07bf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28.0-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:35:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:35:57 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.0`

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

### `docker:28.0.0` - linux; amd64

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

### `docker:28.0.0` - unknown; unknown

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

### `docker:28.0.0` - linux; arm variant v6

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

### `docker:28.0.0` - unknown; unknown

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

### `docker:28.0.0` - linux; arm variant v7

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

### `docker:28.0.0` - unknown; unknown

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

### `docker:28.0.0` - linux; arm64 variant v8

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

### `docker:28.0.0` - unknown; unknown

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

## `docker:28.0.0-alpine3.21`

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

### `docker:28.0.0-alpine3.21` - linux; amd64

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

### `docker:28.0.0-alpine3.21` - unknown; unknown

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

### `docker:28.0.0-alpine3.21` - linux; arm variant v6

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

### `docker:28.0.0-alpine3.21` - unknown; unknown

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

### `docker:28.0.0-alpine3.21` - linux; arm variant v7

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

### `docker:28.0.0-alpine3.21` - unknown; unknown

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

### `docker:28.0.0-alpine3.21` - linux; arm64 variant v8

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

### `docker:28.0.0-alpine3.21` - unknown; unknown

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

## `docker:28.0.0-cli`

```console
$ docker pull docker@sha256:887a9786ad5566037eb9ee72b1c90a90846b385a857258dc06e1e3f6488e43f4
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

### `docker:28.0.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:8cdf18b080fc7b11649280c97dd147c328ea3c82cd09e4e85f0e3e446276d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73936867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ae8bc797f1ebb6b0e032d633fdd9970ca8222fb82f7c5faf28f4d06dd66343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:56e48ba725a90e5447bbbf222ba3b57958dba989c7455400ae0107705fb2edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29702f2c3193de88b7cc798155359414b597aba6cc6e132b4dc6a390229ab5c3`

```dockerfile
```

-	Layers:
	-	`sha256:a0c0c3a81b00183cb3c2d9219542a9321fee1e435151e642f2020bb23037a5e6`  
		Last Modified: Fri, 21 Feb 2025 03:07:42 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:9210cb4fabe4c615183ca805315c7447cfcf89645d7185701451633a9a73abf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68899628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8224895e513dedc9188d6307c9f130dbda5dd94cbf242f25396798350aae5da6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:81cf2965d6ada5e0a87e3e0e5f8aa430e3926d2bac634ca0a11edbaddc4a6e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb96212dc183aff17523a7009a25396a418828fb426f4f7334ca03ff284cc95c`

```dockerfile
```

-	Layers:
	-	`sha256:ede5804b676a2080c79e2f198a3486858b4f9790b3c5b2f3621147fa40edb83e`  
		Last Modified: Fri, 21 Feb 2025 03:07:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:64c3fe7a413de80105071682ae30585431da991cba570aebe1c413afefd63a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67910864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd4097f50aa5e6ca8a005f4ab41aae0743d7ad12ad3c781ed02ccfc5dea7fef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a4622d9c3bec5213e74c5c712b54ae10950233a5e84acc17342dade4cd94f156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba8c3d45c41d43975bf5c1e600922ff8b5d9124c55ac772332087a4cd7bccd4`

```dockerfile
```

-	Layers:
	-	`sha256:8bb09b223df08d8d29f9dce0774ccbd2af9bddac2ad6d4ecc20ee8300d59cd18`  
		Last Modified: Fri, 21 Feb 2025 03:07:44 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dcf2e37500a110aed81793b6a22e21fc806cb1a97ff52ceacd8ac95d20f1363b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f8e9cc2b73b8198319ff8105b4487146527454e6585d3f9cdf92e47a1f6e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0954244e6afa38c31fcb4d785e11c0d073dc1cf43924942c190b998143e00ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd92ef9ae240d50c51adc27276ab23ab1085129b09a03978d52a758c813668c`

```dockerfile
```

-	Layers:
	-	`sha256:2e9175a11d2049bf2a2ba3456fb7de475c4b2595a4404f3a03ea0056a2e4677f`  
		Last Modified: Fri, 21 Feb 2025 03:07:45 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-cli-alpine3.21`

```console
$ docker pull docker@sha256:887a9786ad5566037eb9ee72b1c90a90846b385a857258dc06e1e3f6488e43f4
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

### `docker:28.0.0-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:8cdf18b080fc7b11649280c97dd147c328ea3c82cd09e4e85f0e3e446276d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73936867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ae8bc797f1ebb6b0e032d633fdd9970ca8222fb82f7c5faf28f4d06dd66343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:56e48ba725a90e5447bbbf222ba3b57958dba989c7455400ae0107705fb2edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29702f2c3193de88b7cc798155359414b597aba6cc6e132b4dc6a390229ab5c3`

```dockerfile
```

-	Layers:
	-	`sha256:a0c0c3a81b00183cb3c2d9219542a9321fee1e435151e642f2020bb23037a5e6`  
		Last Modified: Fri, 21 Feb 2025 03:07:42 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:9210cb4fabe4c615183ca805315c7447cfcf89645d7185701451633a9a73abf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68899628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8224895e513dedc9188d6307c9f130dbda5dd94cbf242f25396798350aae5da6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:81cf2965d6ada5e0a87e3e0e5f8aa430e3926d2bac634ca0a11edbaddc4a6e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb96212dc183aff17523a7009a25396a418828fb426f4f7334ca03ff284cc95c`

```dockerfile
```

-	Layers:
	-	`sha256:ede5804b676a2080c79e2f198a3486858b4f9790b3c5b2f3621147fa40edb83e`  
		Last Modified: Fri, 21 Feb 2025 03:07:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:64c3fe7a413de80105071682ae30585431da991cba570aebe1c413afefd63a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67910864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd4097f50aa5e6ca8a005f4ab41aae0743d7ad12ad3c781ed02ccfc5dea7fef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:a4622d9c3bec5213e74c5c712b54ae10950233a5e84acc17342dade4cd94f156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba8c3d45c41d43975bf5c1e600922ff8b5d9124c55ac772332087a4cd7bccd4`

```dockerfile
```

-	Layers:
	-	`sha256:8bb09b223df08d8d29f9dce0774ccbd2af9bddac2ad6d4ecc20ee8300d59cd18`  
		Last Modified: Fri, 21 Feb 2025 03:07:44 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dcf2e37500a110aed81793b6a22e21fc806cb1a97ff52ceacd8ac95d20f1363b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f8e9cc2b73b8198319ff8105b4487146527454e6585d3f9cdf92e47a1f6e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.0.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:0954244e6afa38c31fcb4d785e11c0d073dc1cf43924942c190b998143e00ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd92ef9ae240d50c51adc27276ab23ab1085129b09a03978d52a758c813668c`

```dockerfile
```

-	Layers:
	-	`sha256:2e9175a11d2049bf2a2ba3456fb7de475c4b2595a4404f3a03ea0056a2e4677f`  
		Last Modified: Fri, 21 Feb 2025 03:07:45 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-dind`

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

### `docker:28.0.0-dind` - linux; amd64

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

### `docker:28.0.0-dind` - unknown; unknown

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

### `docker:28.0.0-dind` - linux; arm variant v6

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

### `docker:28.0.0-dind` - unknown; unknown

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

### `docker:28.0.0-dind` - linux; arm variant v7

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

### `docker:28.0.0-dind` - unknown; unknown

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

### `docker:28.0.0-dind` - linux; arm64 variant v8

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

### `docker:28.0.0-dind` - unknown; unknown

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

## `docker:28.0.0-dind-alpine3.21`

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

### `docker:28.0.0-dind-alpine3.21` - linux; amd64

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

### `docker:28.0.0-dind-alpine3.21` - unknown; unknown

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

### `docker:28.0.0-dind-alpine3.21` - linux; arm variant v6

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

### `docker:28.0.0-dind-alpine3.21` - unknown; unknown

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

### `docker:28.0.0-dind-alpine3.21` - linux; arm variant v7

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

### `docker:28.0.0-dind-alpine3.21` - unknown; unknown

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

### `docker:28.0.0-dind-alpine3.21` - linux; arm64 variant v8

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

### `docker:28.0.0-dind-alpine3.21` - unknown; unknown

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

## `docker:28.0.0-dind-rootless`

```console
$ docker pull docker@sha256:c2bdebd237ff73eb4cd004c3d06b91266c8e71fc0eb50cc05b7141f48da9c09b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:baeccb921bfefe9c0abbaf4c27899cc82a1ae8ef8b0bb6647f15ff19a26f1edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159110162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28922b4b7da0159cbf39d0f3a53b9f370655bc0bbdc2253fba400c65b1089dbe`
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
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
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
	-	`sha256:3c751079331c0d7cc77480ccc642bc7a155d54c6407ca58d109a4778a1d219d2`  
		Last Modified: Fri, 21 Feb 2025 01:07:58 GMT  
		Size: 986.6 KB (986567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abccb6ae0375cfd973e871cf8d9498f1137b801e03a1247896fef51459e842b`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279c452f347f576f445fcf89a42c79cef749c5ebf56f8654cb408c36b72596d`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f130ec6bab014d4e4217287e6a9e8ab3c9654578a2d7b81bd9e802b5348cdab`  
		Last Modified: Fri, 21 Feb 2025 01:08:06 GMT  
		Size: 17.2 MB (17166410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6167de8683d8d2c2fcdd7ccb8ebdd22f6b74a4c0c5b83a37d19baaec3c03c`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9b955e2017dc28a3f65f19a930b1245d79fc50869bcf22fb8b9c913bb3651ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb37c52b27e1569e14a67a20fae6f966ceb6926a5abbc2caf93ddc13d67f3430`

```dockerfile
```

-	Layers:
	-	`sha256:6ead672c435cbfcda4dc2151539470781c44ee6fe14e6aeb54abde9de0a82dcc`  
		Last Modified: Fri, 21 Feb 2025 03:07:51 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f8c1cb5a95beb1d7b5b9b55eb239c8e6faf24d0165eefcf3f043e6ed79d64afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152646612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2b5c4ab8d0497964a390eff576c882a14316c7c91817e4f79a67643a89aff9`
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
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
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
	-	`sha256:9f29180dea49ae66c7bc7926ee0ccd3bef65d1fabf038525fa152b1bad745f06`  
		Last Modified: Fri, 21 Feb 2025 01:07:52 GMT  
		Size: 1.0 MB (1014193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc68779566c657f24c79525ad9dcd5c9ee3ffcf02ec3c46a5cda60769586c2f`  
		Last Modified: Fri, 21 Feb 2025 01:07:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc41d26c599adbd498428291a25daa08bec1d395f5041788675dc4b6d6e912ae`  
		Last Modified: Fri, 21 Feb 2025 01:07:47 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9644daeeb7cd964b27d9fb1da77a254ecb25c2c25b5af0ca854b2d116ce08`  
		Last Modified: Fri, 21 Feb 2025 01:08:01 GMT  
		Size: 19.3 MB (19279435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f32d46f74022d488c81b4699aacff888d0301c2604d5665e93a34637c0742c7`  
		Last Modified: Fri, 21 Feb 2025 01:07:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:678f2f3f2fb1f6f4f47993ee1e513d82b0bf087173fa5d5ea2959690983a29c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fcb6725765cad4c7473f3e074b75927da8619de4e33f364720a8516ba1ac21`

```dockerfile
```

-	Layers:
	-	`sha256:5fe70a257c51d2754ab1d2db0953e9c3dd069fc47ea471e1c648a72885f409b3`  
		Last Modified: Fri, 21 Feb 2025 03:07:52 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-windowsservercore`

```console
$ docker pull docker@sha256:42bea6bfadb1655060b67b4af39235b2befa0d07799d5348506e6b43682b0af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:28.0.0-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:35:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:35:57 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.0-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:8c87e235530294d2b88d865e9b73352d741bf135bb5d7996357cc1259e792013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328621027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8baca22cc4eb365396c38a0c864ca7ce92d7a6a9f746db6704272ddb0e3b282`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 20 Feb 2025 23:38:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:39:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:39:21 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:39:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:39:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fea355b62ca4572b994dc74c2715f6d0e572dee1dde122c1b9667ba29a52bc`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4add6994a30cf2372676e5f6dcc501322c314740cbbaa81aedfd7f34fd114`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 365.4 KB (365409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfeb2a4441074cfb72ba4bbfb54d10e780fed5ebd4282f5aabb1d10a001b29b`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f37810d123d73eb77f2e07547d933af7005c60006ef944be2dc10aef6324ed7`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3cd08c82763ba826aa7f7c8e2fb0f7d38ded99fa8ceeb30dd0ed7c9fd2e2cf`  
		Last Modified: Thu, 20 Feb 2025 23:41:05 GMT  
		Size: 19.8 MB (19808968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad43392a0fb22c04f2fa5cf91d4e11ec2a6c1ade3934b213ebf918efa33e68`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2b5ed6114086b1deb97a464286804f8378784b8a76534f433dd3af1e5e706`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bc64e43a7efc1920189c900466e96f283a332d8c1a3a72cd6faa9e058dc37f`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eea4a39141050304ffd8c8247b3cb3779dbe12b30c278321f2454c7880a504`  
		Last Modified: Thu, 20 Feb 2025 23:41:16 GMT  
		Size: 22.7 MB (22747811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4b9a6967d16d3acceb3fdb5931bc90756517ecfa050319e2ac963a3a103a1`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21b04e127078d780548cf476f502da6ea984f45478286b4442eec97295207a`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053a644814e3f4033758fd3178c1a08ec78ce6d25c0942cdf4e18465a756517`  
		Last Modified: Thu, 20 Feb 2025 23:41:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c4aa754555e50ae5def00c6bafb9a987221023c5e0f47dd1c064adf20dbf9`  
		Last Modified: Thu, 20 Feb 2025 23:41:17 GMT  
		Size: 21.8 MB (21829214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.0-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:50d0bfde03e0b6f40598d31e004c4bb2403a80c9fff9f3934f2cd9f4727dabe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201683757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41ca21d8b613f4b46e76253dc47469b785006575cbbfa3f3e710f82a7cefdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 20 Feb 2025 23:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:37:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:37:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:37:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:37:32 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:37:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7a1d363a7cbc76c8803b0b2bfe5892407eef1a2c8f2a703812077cca802fb`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68969c343b72ab00102b3454a5042bcddfe3b4e214ca6b9f25c1054157bf873f`  
		Last Modified: Thu, 20 Feb 2025 23:38:44 GMT  
		Size: 356.6 KB (356613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd531517a87fb70100fecd706d41d299866177bd6e79eaef5172574a94e5127f`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac190ca9022227c882e04edfe0565f94fc3ea450ed8ed03fcfc10cb7e3a78ed`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630d6ec4dd535487f3145d617fe15227b850ecebc3613240658f71f4cf41486`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 19.8 MB (19818182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2275ba90e41fea0e66b50f7e6e5c34e084b069ecdefa9a42a7841db475798`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22539d4654b28662e6c4e0bd90de707de4d9815125015add8119448b286ef`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ede31d628f2b1abb82df21bfe3df1b33777312763d138c5c6039a6836608bf`  
		Last Modified: Thu, 20 Feb 2025 23:38:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08e15c1d44c604540ec54984f8dc55dd1d8ce7b7f7022714e63aa0d4c657eb0`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 22.8 MB (22756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce614b28a9ab99b1233346d2807b68b6369e28e3dd2a09189393474c522c92a`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74939f5df35bb4dc1e17acd099963211f6438d8871b89c20864b13fe92c47`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c24f4a68afc8435ccb724cefc8d7c92e0411f2123301aa269ecce5ef8319ba`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2860f40f04ae4699daca17122267a4f8c37df8e61f22a5ef5552029d29feb`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 21.8 MB (21831256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:129835b071beea9e35dbec8b6c134b387ff94e9f28e7b92a74079c74cb2812d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:28.0.0-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:50d0bfde03e0b6f40598d31e004c4bb2403a80c9fff9f3934f2cd9f4727dabe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201683757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41ca21d8b613f4b46e76253dc47469b785006575cbbfa3f3e710f82a7cefdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 20 Feb 2025 23:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:37:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:37:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:37:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:37:32 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:37:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7a1d363a7cbc76c8803b0b2bfe5892407eef1a2c8f2a703812077cca802fb`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68969c343b72ab00102b3454a5042bcddfe3b4e214ca6b9f25c1054157bf873f`  
		Last Modified: Thu, 20 Feb 2025 23:38:44 GMT  
		Size: 356.6 KB (356613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd531517a87fb70100fecd706d41d299866177bd6e79eaef5172574a94e5127f`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac190ca9022227c882e04edfe0565f94fc3ea450ed8ed03fcfc10cb7e3a78ed`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630d6ec4dd535487f3145d617fe15227b850ecebc3613240658f71f4cf41486`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 19.8 MB (19818182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2275ba90e41fea0e66b50f7e6e5c34e084b069ecdefa9a42a7841db475798`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22539d4654b28662e6c4e0bd90de707de4d9815125015add8119448b286ef`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ede31d628f2b1abb82df21bfe3df1b33777312763d138c5c6039a6836608bf`  
		Last Modified: Thu, 20 Feb 2025 23:38:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08e15c1d44c604540ec54984f8dc55dd1d8ce7b7f7022714e63aa0d4c657eb0`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 22.8 MB (22756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce614b28a9ab99b1233346d2807b68b6369e28e3dd2a09189393474c522c92a`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74939f5df35bb4dc1e17acd099963211f6438d8871b89c20864b13fe92c47`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c24f4a68afc8435ccb724cefc8d7c92e0411f2123301aa269ecce5ef8319ba`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2860f40f04ae4699daca17122267a4f8c37df8e61f22a5ef5552029d29feb`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 21.8 MB (21831256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:63142c95c405e1018b42a36af9d368023e4db8ea8d9e9e45d7120f9340348705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:28.0.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:8c87e235530294d2b88d865e9b73352d741bf135bb5d7996357cc1259e792013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328621027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8baca22cc4eb365396c38a0c864ca7ce92d7a6a9f746db6704272ddb0e3b282`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 20 Feb 2025 23:38:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:39:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:39:21 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:39:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:39:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fea355b62ca4572b994dc74c2715f6d0e572dee1dde122c1b9667ba29a52bc`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4add6994a30cf2372676e5f6dcc501322c314740cbbaa81aedfd7f34fd114`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 365.4 KB (365409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfeb2a4441074cfb72ba4bbfb54d10e780fed5ebd4282f5aabb1d10a001b29b`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f37810d123d73eb77f2e07547d933af7005c60006ef944be2dc10aef6324ed7`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3cd08c82763ba826aa7f7c8e2fb0f7d38ded99fa8ceeb30dd0ed7c9fd2e2cf`  
		Last Modified: Thu, 20 Feb 2025 23:41:05 GMT  
		Size: 19.8 MB (19808968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad43392a0fb22c04f2fa5cf91d4e11ec2a6c1ade3934b213ebf918efa33e68`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2b5ed6114086b1deb97a464286804f8378784b8a76534f433dd3af1e5e706`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bc64e43a7efc1920189c900466e96f283a332d8c1a3a72cd6faa9e058dc37f`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eea4a39141050304ffd8c8247b3cb3779dbe12b30c278321f2454c7880a504`  
		Last Modified: Thu, 20 Feb 2025 23:41:16 GMT  
		Size: 22.7 MB (22747811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4b9a6967d16d3acceb3fdb5931bc90756517ecfa050319e2ac963a3a103a1`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21b04e127078d780548cf476f502da6ea984f45478286b4442eec97295207a`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053a644814e3f4033758fd3178c1a08ec78ce6d25c0942cdf4e18465a756517`  
		Last Modified: Thu, 20 Feb 2025 23:41:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c4aa754555e50ae5def00c6bafb9a987221023c5e0f47dd1c064adf20dbf9`  
		Last Modified: Thu, 20 Feb 2025 23:41:17 GMT  
		Size: 21.8 MB (21829214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d99acb3911040c398b54e203664f1bb3f30d631567e6c22f94471cd2a07bf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28.0.0-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:35:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:35:57 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:887a9786ad5566037eb9ee72b1c90a90846b385a857258dc06e1e3f6488e43f4
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
$ docker pull docker@sha256:8cdf18b080fc7b11649280c97dd147c328ea3c82cd09e4e85f0e3e446276d05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73936867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ae8bc797f1ebb6b0e032d633fdd9970ca8222fb82f7c5faf28f4d06dd66343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:56e48ba725a90e5447bbbf222ba3b57958dba989c7455400ae0107705fb2edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29702f2c3193de88b7cc798155359414b597aba6cc6e132b4dc6a390229ab5c3`

```dockerfile
```

-	Layers:
	-	`sha256:a0c0c3a81b00183cb3c2d9219542a9321fee1e435151e642f2020bb23037a5e6`  
		Last Modified: Fri, 21 Feb 2025 03:07:42 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:9210cb4fabe4c615183ca805315c7447cfcf89645d7185701451633a9a73abf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68899628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8224895e513dedc9188d6307c9f130dbda5dd94cbf242f25396798350aae5da6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:81cf2965d6ada5e0a87e3e0e5f8aa430e3926d2bac634ca0a11edbaddc4a6e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb96212dc183aff17523a7009a25396a418828fb426f4f7334ca03ff284cc95c`

```dockerfile
```

-	Layers:
	-	`sha256:ede5804b676a2080c79e2f198a3486858b4f9790b3c5b2f3621147fa40edb83e`  
		Last Modified: Fri, 21 Feb 2025 03:07:43 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:64c3fe7a413de80105071682ae30585431da991cba570aebe1c413afefd63a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67910864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd4097f50aa5e6ca8a005f4ab41aae0743d7ad12ad3c781ed02ccfc5dea7fef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a4622d9c3bec5213e74c5c712b54ae10950233a5e84acc17342dade4cd94f156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba8c3d45c41d43975bf5c1e600922ff8b5d9124c55ac772332087a4cd7bccd4`

```dockerfile
```

-	Layers:
	-	`sha256:8bb09b223df08d8d29f9dce0774ccbd2af9bddac2ad6d4ecc20ee8300d59cd18`  
		Last Modified: Fri, 21 Feb 2025 03:07:44 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dcf2e37500a110aed81793b6a22e21fc806cb1a97ff52ceacd8ac95d20f1363b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f8e9cc2b73b8198319ff8105b4487146527454e6585d3f9cdf92e47a1f6e78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0954244e6afa38c31fcb4d785e11c0d073dc1cf43924942c190b998143e00ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd92ef9ae240d50c51adc27276ab23ab1085129b09a03978d52a758c813668c`

```dockerfile
```

-	Layers:
	-	`sha256:2e9175a11d2049bf2a2ba3456fb7de475c4b2595a4404f3a03ea0056a2e4677f`  
		Last Modified: Fri, 21 Feb 2025 03:07:45 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

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

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:c2bdebd237ff73eb4cd004c3d06b91266c8e71fc0eb50cc05b7141f48da9c09b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:baeccb921bfefe9c0abbaf4c27899cc82a1ae8ef8b0bb6647f15ff19a26f1edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159110162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28922b4b7da0159cbf39d0f3a53b9f370655bc0bbdc2253fba400c65b1089dbe`
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
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
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
	-	`sha256:3c751079331c0d7cc77480ccc642bc7a155d54c6407ca58d109a4778a1d219d2`  
		Last Modified: Fri, 21 Feb 2025 01:07:58 GMT  
		Size: 986.6 KB (986567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abccb6ae0375cfd973e871cf8d9498f1137b801e03a1247896fef51459e842b`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279c452f347f576f445fcf89a42c79cef749c5ebf56f8654cb408c36b72596d`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f130ec6bab014d4e4217287e6a9e8ab3c9654578a2d7b81bd9e802b5348cdab`  
		Last Modified: Fri, 21 Feb 2025 01:08:06 GMT  
		Size: 17.2 MB (17166410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6167de8683d8d2c2fcdd7ccb8ebdd22f6b74a4c0c5b83a37d19baaec3c03c`  
		Last Modified: Fri, 21 Feb 2025 01:07:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9b955e2017dc28a3f65f19a930b1245d79fc50869bcf22fb8b9c913bb3651ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb37c52b27e1569e14a67a20fae6f966ceb6926a5abbc2caf93ddc13d67f3430`

```dockerfile
```

-	Layers:
	-	`sha256:6ead672c435cbfcda4dc2151539470781c44ee6fe14e6aeb54abde9de0a82dcc`  
		Last Modified: Fri, 21 Feb 2025 03:07:51 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f8c1cb5a95beb1d7b5b9b55eb239c8e6faf24d0165eefcf3f043e6ed79d64afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152646612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2b5c4ab8d0497964a390eff576c882a14316c7c91817e4f79a67643a89aff9`
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
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
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
	-	`sha256:9f29180dea49ae66c7bc7926ee0ccd3bef65d1fabf038525fa152b1bad745f06`  
		Last Modified: Fri, 21 Feb 2025 01:07:52 GMT  
		Size: 1.0 MB (1014193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc68779566c657f24c79525ad9dcd5c9ee3ffcf02ec3c46a5cda60769586c2f`  
		Last Modified: Fri, 21 Feb 2025 01:07:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc41d26c599adbd498428291a25daa08bec1d395f5041788675dc4b6d6e912ae`  
		Last Modified: Fri, 21 Feb 2025 01:07:47 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9644daeeb7cd964b27d9fb1da77a254ecb25c2c25b5af0ca854b2d116ce08`  
		Last Modified: Fri, 21 Feb 2025 01:08:01 GMT  
		Size: 19.3 MB (19279435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f32d46f74022d488c81b4699aacff888d0301c2604d5665e93a34637c0742c7`  
		Last Modified: Fri, 21 Feb 2025 01:07:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:678f2f3f2fb1f6f4f47993ee1e513d82b0bf087173fa5d5ea2959690983a29c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fcb6725765cad4c7473f3e074b75927da8619de4e33f364720a8516ba1ac21`

```dockerfile
```

-	Layers:
	-	`sha256:5fe70a257c51d2754ab1d2db0953e9c3dd069fc47ea471e1c648a72885f409b3`  
		Last Modified: Fri, 21 Feb 2025 03:07:52 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

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

### `docker:latest` - linux; amd64

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

### `docker:latest` - unknown; unknown

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

### `docker:latest` - linux; arm variant v6

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

### `docker:latest` - unknown; unknown

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

### `docker:latest` - linux; arm variant v7

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

### `docker:latest` - unknown; unknown

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

### `docker:latest` - linux; arm64 variant v8

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

### `docker:latest` - unknown; unknown

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

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:42bea6bfadb1655060b67b4af39235b2befa0d07799d5348506e6b43682b0af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:35:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:35:57 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:8c87e235530294d2b88d865e9b73352d741bf135bb5d7996357cc1259e792013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328621027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8baca22cc4eb365396c38a0c864ca7ce92d7a6a9f746db6704272ddb0e3b282`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 20 Feb 2025 23:38:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:39:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:39:21 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:39:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:39:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fea355b62ca4572b994dc74c2715f6d0e572dee1dde122c1b9667ba29a52bc`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4add6994a30cf2372676e5f6dcc501322c314740cbbaa81aedfd7f34fd114`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 365.4 KB (365409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfeb2a4441074cfb72ba4bbfb54d10e780fed5ebd4282f5aabb1d10a001b29b`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f37810d123d73eb77f2e07547d933af7005c60006ef944be2dc10aef6324ed7`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3cd08c82763ba826aa7f7c8e2fb0f7d38ded99fa8ceeb30dd0ed7c9fd2e2cf`  
		Last Modified: Thu, 20 Feb 2025 23:41:05 GMT  
		Size: 19.8 MB (19808968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad43392a0fb22c04f2fa5cf91d4e11ec2a6c1ade3934b213ebf918efa33e68`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2b5ed6114086b1deb97a464286804f8378784b8a76534f433dd3af1e5e706`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bc64e43a7efc1920189c900466e96f283a332d8c1a3a72cd6faa9e058dc37f`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eea4a39141050304ffd8c8247b3cb3779dbe12b30c278321f2454c7880a504`  
		Last Modified: Thu, 20 Feb 2025 23:41:16 GMT  
		Size: 22.7 MB (22747811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4b9a6967d16d3acceb3fdb5931bc90756517ecfa050319e2ac963a3a103a1`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21b04e127078d780548cf476f502da6ea984f45478286b4442eec97295207a`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053a644814e3f4033758fd3178c1a08ec78ce6d25c0942cdf4e18465a756517`  
		Last Modified: Thu, 20 Feb 2025 23:41:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c4aa754555e50ae5def00c6bafb9a987221023c5e0f47dd1c064adf20dbf9`  
		Last Modified: Thu, 20 Feb 2025 23:41:17 GMT  
		Size: 21.8 MB (21829214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:50d0bfde03e0b6f40598d31e004c4bb2403a80c9fff9f3934f2cd9f4727dabe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201683757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41ca21d8b613f4b46e76253dc47469b785006575cbbfa3f3e710f82a7cefdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 20 Feb 2025 23:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:37:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:37:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:37:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:37:32 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:37:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7a1d363a7cbc76c8803b0b2bfe5892407eef1a2c8f2a703812077cca802fb`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68969c343b72ab00102b3454a5042bcddfe3b4e214ca6b9f25c1054157bf873f`  
		Last Modified: Thu, 20 Feb 2025 23:38:44 GMT  
		Size: 356.6 KB (356613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd531517a87fb70100fecd706d41d299866177bd6e79eaef5172574a94e5127f`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac190ca9022227c882e04edfe0565f94fc3ea450ed8ed03fcfc10cb7e3a78ed`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630d6ec4dd535487f3145d617fe15227b850ecebc3613240658f71f4cf41486`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 19.8 MB (19818182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2275ba90e41fea0e66b50f7e6e5c34e084b069ecdefa9a42a7841db475798`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22539d4654b28662e6c4e0bd90de707de4d9815125015add8119448b286ef`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ede31d628f2b1abb82df21bfe3df1b33777312763d138c5c6039a6836608bf`  
		Last Modified: Thu, 20 Feb 2025 23:38:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08e15c1d44c604540ec54984f8dc55dd1d8ce7b7f7022714e63aa0d4c657eb0`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 22.8 MB (22756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce614b28a9ab99b1233346d2807b68b6369e28e3dd2a09189393474c522c92a`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74939f5df35bb4dc1e17acd099963211f6438d8871b89c20864b13fe92c47`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c24f4a68afc8435ccb724cefc8d7c92e0411f2123301aa269ecce5ef8319ba`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2860f40f04ae4699daca17122267a4f8c37df8e61f22a5ef5552029d29feb`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 21.8 MB (21831256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:129835b071beea9e35dbec8b6c134b387ff94e9f28e7b92a74079c74cb2812d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:50d0bfde03e0b6f40598d31e004c4bb2403a80c9fff9f3934f2cd9f4727dabe1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201683757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41ca21d8b613f4b46e76253dc47469b785006575cbbfa3f3e710f82a7cefdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 20 Feb 2025 23:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:37:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:37:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:37:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:30 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:37:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:37:32 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:37:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:37:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:37:42 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e7a1d363a7cbc76c8803b0b2bfe5892407eef1a2c8f2a703812077cca802fb`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68969c343b72ab00102b3454a5042bcddfe3b4e214ca6b9f25c1054157bf873f`  
		Last Modified: Thu, 20 Feb 2025 23:38:44 GMT  
		Size: 356.6 KB (356613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd531517a87fb70100fecd706d41d299866177bd6e79eaef5172574a94e5127f`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac190ca9022227c882e04edfe0565f94fc3ea450ed8ed03fcfc10cb7e3a78ed`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630d6ec4dd535487f3145d617fe15227b850ecebc3613240658f71f4cf41486`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 19.8 MB (19818182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2275ba90e41fea0e66b50f7e6e5c34e084b069ecdefa9a42a7841db475798`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22539d4654b28662e6c4e0bd90de707de4d9815125015add8119448b286ef`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ede31d628f2b1abb82df21bfe3df1b33777312763d138c5c6039a6836608bf`  
		Last Modified: Thu, 20 Feb 2025 23:38:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08e15c1d44c604540ec54984f8dc55dd1d8ce7b7f7022714e63aa0d4c657eb0`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 22.8 MB (22756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce614b28a9ab99b1233346d2807b68b6369e28e3dd2a09189393474c522c92a`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74939f5df35bb4dc1e17acd099963211f6438d8871b89c20864b13fe92c47`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c24f4a68afc8435ccb724cefc8d7c92e0411f2123301aa269ecce5ef8319ba`  
		Last Modified: Thu, 20 Feb 2025 23:38:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2860f40f04ae4699daca17122267a4f8c37df8e61f22a5ef5552029d29feb`  
		Last Modified: Thu, 20 Feb 2025 23:38:54 GMT  
		Size: 21.8 MB (21831256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:63142c95c405e1018b42a36af9d368023e4db8ea8d9e9e45d7120f9340348705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:8c87e235530294d2b88d865e9b73352d741bf135bb5d7996357cc1259e792013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328621027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8baca22cc4eb365396c38a0c864ca7ce92d7a6a9f746db6704272ddb0e3b282`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 20 Feb 2025 23:38:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:39:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:39:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:39:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:39:21 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:39:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:39:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:39:30 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:39:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fea355b62ca4572b994dc74c2715f6d0e572dee1dde122c1b9667ba29a52bc`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b4add6994a30cf2372676e5f6dcc501322c314740cbbaa81aedfd7f34fd114`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 365.4 KB (365409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfeb2a4441074cfb72ba4bbfb54d10e780fed5ebd4282f5aabb1d10a001b29b`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f37810d123d73eb77f2e07547d933af7005c60006ef944be2dc10aef6324ed7`  
		Last Modified: Thu, 20 Feb 2025 23:41:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3cd08c82763ba826aa7f7c8e2fb0f7d38ded99fa8ceeb30dd0ed7c9fd2e2cf`  
		Last Modified: Thu, 20 Feb 2025 23:41:05 GMT  
		Size: 19.8 MB (19808968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad43392a0fb22c04f2fa5cf91d4e11ec2a6c1ade3934b213ebf918efa33e68`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2b5ed6114086b1deb97a464286804f8378784b8a76534f433dd3af1e5e706`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bc64e43a7efc1920189c900466e96f283a332d8c1a3a72cd6faa9e058dc37f`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eea4a39141050304ffd8c8247b3cb3779dbe12b30c278321f2454c7880a504`  
		Last Modified: Thu, 20 Feb 2025 23:41:16 GMT  
		Size: 22.7 MB (22747811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4b9a6967d16d3acceb3fdb5931bc90756517ecfa050319e2ac963a3a103a1`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21b04e127078d780548cf476f502da6ea984f45478286b4442eec97295207a`  
		Last Modified: Thu, 20 Feb 2025 23:41:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053a644814e3f4033758fd3178c1a08ec78ce6d25c0942cdf4e18465a756517`  
		Last Modified: Thu, 20 Feb 2025 23:41:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c4aa754555e50ae5def00c6bafb9a987221023c5e0f47dd1c064adf20dbf9`  
		Last Modified: Thu, 20 Feb 2025 23:41:17 GMT  
		Size: 21.8 MB (21829214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d99acb3911040c398b54e203664f1bb3f30d631567e6c22f94471cd2a07bf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:35:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:35:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:35:57 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:35:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:35:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:35:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:35:59 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
