## `docker:29-cli`

```console
$ docker pull docker@sha256:06a1ee7af01fecf797268686773f20d1410a8ef4da497144bd08001011b1fffa
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

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:d6d7d49911a0c8f2c5b75eb82e41d16df8a1ce886386dfda2ca0a52c3573955f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64719277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1854aeb6cfc4a2f0e4632a6a02e1a83509e0c147cb657c302fb0de928ae07969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 19:03:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 09 Jan 2026 19:03:48 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 09 Jan 2026 19:03:48 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 09 Jan 2026 19:04:10 GMT
ENV DOCKER_VERSION=29.1.4
# Fri, 09 Jan 2026 19:04:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 09 Jan 2026 19:04:10 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 09 Jan 2026 19:04:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 09 Jan 2026 19:04:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 09 Jan 2026 19:04:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 09 Jan 2026 19:04:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 09 Jan 2026 19:04:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:04:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 09 Jan 2026 19:04:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 09 Jan 2026 19:04:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:04:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb62aaf497bdaab35bd5654be0ded1a723529328bc67b53299be81ce21f4faa`  
		Last Modified: Fri, 09 Jan 2026 19:04:08 GMT  
		Size: 8.4 MB (8399655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75e5841aad023dc9bf9c9ec7e0ec516d4606823af36e39a9aa6cc79bdbac2a2`  
		Last Modified: Fri, 09 Jan 2026 19:04:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324a34400dd3321e8c94651e8dc80411d403e2f457eb20f717128576c5804c2d`  
		Last Modified: Fri, 09 Jan 2026 19:04:28 GMT  
		Size: 18.8 MB (18764492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7cf0400db94887ce8d1185bcaa2825939e5f761f00460cdab3ec9feb30357`  
		Last Modified: Fri, 09 Jan 2026 19:04:28 GMT  
		Size: 22.9 MB (22905497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca227cbf4720b9fa3aa4967e1349f88b60ab71f2f2aa6228b11a171c644f66`  
		Last Modified: Fri, 09 Jan 2026 19:04:26 GMT  
		Size: 10.8 MB (10787385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528890f01b0f88d18148e0587b9dbe0e52d1253b2e0111c9b05b9e2ec42687e3`  
		Last Modified: Fri, 09 Jan 2026 19:04:25 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dced782f1cc36add133c0a8c8e169999a16cf080c9dfafd704321742d188f86`  
		Last Modified: Fri, 09 Jan 2026 19:04:26 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394ce473e2db61875059956f88e17c9849fc2fc6e6f1d87f359d80f2207cfa6a`  
		Last Modified: Fri, 09 Jan 2026 19:04:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2d236ee7aabb8213ca8ee06fbbaf988228111149b57922fa1045178c2c9412b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad80716b25d923b80c375d12365e3cdcf17e46ceacf2654b43300723e363e7e`

```dockerfile
```

-	Layers:
	-	`sha256:3126e43910c12a2d780191550e21f1969b3265b3a4c27d50b61b7e668ad056fc`  
		Last Modified: Fri, 09 Jan 2026 21:07:37 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:0986635805cb349e00144c9bd9df1032330c1be658abb81948797bb511094a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61108672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0c7b590df55c772803db6d1a5115e87d01b510f37190c033635289b343e2b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 21:59:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 09 Jan 2026 21:59:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 09 Jan 2026 21:59:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 09 Jan 2026 21:59:16 GMT
ENV DOCKER_VERSION=29.1.4
# Fri, 09 Jan 2026 21:59:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 09 Jan 2026 21:59:16 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 09 Jan 2026 21:59:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 09 Jan 2026 21:59:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 09 Jan 2026 21:59:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 09 Jan 2026 21:59:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 09 Jan 2026 21:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 21:59:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 09 Jan 2026 21:59:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 09 Jan 2026 21:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 21:59:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe434dd0bfb7364e8b6d4e15b673e0c1f213de54849ece79dc71692525a664ad`  
		Last Modified: Fri, 09 Jan 2026 21:59:35 GMT  
		Size: 8.3 MB (8300970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75492969e28b1178dd6417c916ae436910b3e270cee055a812233c66516b7d90`  
		Last Modified: Fri, 09 Jan 2026 21:59:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcef08ad0fed9e5bc436f4aa268ccd17f4b99b3c6db560cb1ef8e2647de8d3a6`  
		Last Modified: Fri, 09 Jan 2026 21:59:26 GMT  
		Size: 17.6 MB (17563699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef53fcb18a69ccf9a5a0b9ff4dad51d4be894de956a5b073dbf97056b3c76f4`  
		Last Modified: Fri, 09 Jan 2026 21:59:34 GMT  
		Size: 21.5 MB (21476551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f040b88ad1b5858361cb8410ce2c737ccba10e8065706a6c7a76e5272ba47`  
		Last Modified: Fri, 09 Jan 2026 21:59:35 GMT  
		Size: 10.2 MB (10196873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6bd787887804f153ab62d8ee8da8b5cbce2c39289d9bf89944300c903084a9`  
		Last Modified: Fri, 09 Jan 2026 21:59:33 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39baf3850d959eaa55d0af02827511ba001a289c6ce579e921915a527d88b479`  
		Last Modified: Fri, 09 Jan 2026 21:59:33 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed02a8089ec02f2f512166c0dd74be2bde9ee59210c0c68db3b90cb697d3d58`  
		Last Modified: Fri, 09 Jan 2026 21:59:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:47f7d03bd99731851df4952f353eaa2cd84fec2bef7aa336f670c75971a9f00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1abccddc11b970529677e2239de710fcc9173925da00ad970920d0b2914378`

```dockerfile
```

-	Layers:
	-	`sha256:d2bda856ce496b06995ec7aa104ff2d3154ac5b0963a20ab8e70227ca4ebb3ce`  
		Last Modified: Sat, 10 Jan 2026 00:07:47 GMT  
		Size: 38.2 KB (38221 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:bad0d78b7399cf06e696b3a8c4c22fd174e13bf9a97061324d176c5f531a2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60075411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092bb312e80805d2587e36a2bd7ca43ea1a4deeec1a845cbd58ebdfcc4262ef6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 19:07:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 09 Jan 2026 19:07:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 09 Jan 2026 19:07:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 09 Jan 2026 19:07:56 GMT
ENV DOCKER_VERSION=29.1.4
# Fri, 09 Jan 2026 19:07:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 09 Jan 2026 19:07:56 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 09 Jan 2026 19:07:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 09 Jan 2026 19:07:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 09 Jan 2026 19:08:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 09 Jan 2026 19:08:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 09 Jan 2026 19:08:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:08:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 09 Jan 2026 19:08:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 09 Jan 2026 19:08:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:08:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df34ee5f3a644608b8629510ecb9d3c6a270106e631ab6cd89cb0d986e2548d`  
		Last Modified: Fri, 09 Jan 2026 19:08:15 GMT  
		Size: 7.6 MB (7597816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8026542e43b1c45a277841cc7766195582bc6a5b75b2b721329faab9c8b1ba`  
		Last Modified: Fri, 09 Jan 2026 19:08:14 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c3033a43799b21a3a47800aa963844c32d0f5df15a8d18bbf9f6b9abeddaf8`  
		Last Modified: Fri, 09 Jan 2026 19:08:17 GMT  
		Size: 17.6 MB (17551652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b591707d98c8855c2ddbf78a2fb982469f0dc3a43f7dd22d9f576e27f35c78`  
		Last Modified: Fri, 09 Jan 2026 19:08:18 GMT  
		Size: 21.5 MB (21454900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa25a2484ec2451677a86e579d36d41d5a13c52dd37ed2f67a0439603ca1be`  
		Last Modified: Fri, 09 Jan 2026 19:08:16 GMT  
		Size: 10.2 MB (10189504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a0aa9795b7359e978e31a26599305e7159398413029ee1dacc0d3d6310038b`  
		Last Modified: Fri, 09 Jan 2026 19:08:14 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77d7e8de73a3ed357ecc0c37ed99e00b09a81b0a1ee3605ebd277100eec38d1`  
		Last Modified: Fri, 09 Jan 2026 19:08:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f9709c75371ba7818835bb40a9c62b4ad7a1a9048167b96660e6606f443922`  
		Last Modified: Fri, 09 Jan 2026 19:08:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d3747c130f39fac122ef2a84b1aaf55558d3b70bcbfece912a56ec07feec1ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f95fbb02c1b9c1ab8dbbd4d61671217984190833dd8cbd5c2ea8dafe9cea68`

```dockerfile
```

-	Layers:
	-	`sha256:d710fded6d5f2d93f4d20ba2b1d76974c1ca2c58ebe81f3637c7ae47dd577eba`  
		Last Modified: Fri, 09 Jan 2026 21:07:42 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d0ca4a66c3de9143d0318dddab0c026274046d2608ac6eea75fbde80d2d49c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60576218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e46ebb29acc270db7c3de7c612f422701b697d8d63316dcc6af9e0cf3dca3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 19:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 09 Jan 2026 19:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 09 Jan 2026 19:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 09 Jan 2026 19:04:39 GMT
ENV DOCKER_VERSION=29.1.4
# Fri, 09 Jan 2026 19:04:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 09 Jan 2026 19:04:39 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 09 Jan 2026 19:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 09 Jan 2026 19:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 09 Jan 2026 19:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 09 Jan 2026 19:04:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 09 Jan 2026 19:04:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:04:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 09 Jan 2026 19:04:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 09 Jan 2026 19:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:04:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f8bf3dd8fa8528642b7f942826595a968992f59707c58be3bdfa183bc25051`  
		Last Modified: Fri, 09 Jan 2026 19:04:35 GMT  
		Size: 8.5 MB (8453498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9542a91f4ad3bcdd3bde7d2d52ab0f8fc6c687637cb74d8db48eb6f854d2516`  
		Last Modified: Fri, 09 Jan 2026 19:04:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebad76b76f7ac7c5fe028cd2bc6d8fb2cf9d125cdd0c87d8149e7f5c8fe33384`  
		Last Modified: Fri, 09 Jan 2026 19:04:55 GMT  
		Size: 17.3 MB (17337570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c148e973a7a9e34f642997a9b985c90374fa1fcf67ecf2d5d0295896a77b918a`  
		Last Modified: Fri, 09 Jan 2026 19:04:55 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c182f8a4df0decc7eee701881284899d19bde065ab7a481e0865308978fbc943`  
		Last Modified: Fri, 09 Jan 2026 19:04:57 GMT  
		Size: 9.9 MB (9942181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf59bc70c4d429a4cffb2440a5594b6a9082bd8a8155bae3e5604295289cbb56`  
		Last Modified: Fri, 09 Jan 2026 19:04:53 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5f10388b43ba17c1a4630721d8c27019634be6e7967f1bbe97542350cbf096`  
		Last Modified: Fri, 09 Jan 2026 19:04:54 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42e86a9eafb17d2f8abe5180d00ef1e65d38fb1f9d386f3bf042d744b55035e`  
		Last Modified: Fri, 09 Jan 2026 19:04:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8f76aed0219fb3c4d6bfe34226edd9688018a3405dd589ddbdc6925fb7d248ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a656aa08205f4e97836fef6a3f4bd2fc6bccdbe848bd8894262301434e6154`

```dockerfile
```

-	Layers:
	-	`sha256:4845e9b07d9a58aa47f16f87d120dc438dedf1b0c38b86207c4f35d4ffec5810`  
		Last Modified: Fri, 09 Jan 2026 21:07:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json
