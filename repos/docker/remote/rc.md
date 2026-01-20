## `docker:rc`

```console
$ docker pull docker@sha256:0e98593319b06c1b54cab0f3842525e515c4cd4983177c30324d25d92da67215
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

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:7e9f23c25fb6b0393b1dd4773192622abf64c9fa8108d08861039d76f146f9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137510418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e70eeabc841f0c3565599d41be043e0aa8b027a0dca00cb9c79874f62689c9a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

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
# Fri, 09 Jan 2026 19:03:50 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Fri, 09 Jan 2026 19:03:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 09 Jan 2026 19:03:50 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 09 Jan 2026 19:03:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 09 Jan 2026 19:03:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 09 Jan 2026 19:03:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 09 Jan 2026 19:03:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 09 Jan 2026 19:03:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:03:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 09 Jan 2026 19:03:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 09 Jan 2026 19:03:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:03:51 GMT
CMD ["sh"]
# Fri, 09 Jan 2026 19:08:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 09 Jan 2026 19:08:04 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 09 Jan 2026 19:08:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 09 Jan 2026 19:08:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 09 Jan 2026 19:08:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 09 Jan 2026 19:08:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 09 Jan 2026 19:08:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:08:07 GMT
VOLUME [/var/lib/docker]
# Fri, 09 Jan 2026 19:08:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 09 Jan 2026 19:08:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 09 Jan 2026 19:08:07 GMT
CMD []
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
		Last Modified: Fri, 09 Jan 2026 19:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0fe8e97b533ec0331c305cf4b9fe77e9c19587b72618a96b126cfd11edd2b`  
		Last Modified: Fri, 09 Jan 2026 19:04:10 GMT  
		Size: 18.8 MB (18766132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240540f6c397db81e33375c238870701ff290db4e85169583e18d9e9a1ac6ef`  
		Last Modified: Fri, 09 Jan 2026 19:03:59 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc3c6f1b3144f6d7ced5090d3583612f728d942ea3347bd8dce88d07187786f`  
		Last Modified: Fri, 09 Jan 2026 19:04:08 GMT  
		Size: 10.8 MB (10787393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee6f08f36a29668fba7c39242e2a198dca85a3f86ecc612bd1bfe580ace45fa`  
		Last Modified: Fri, 09 Jan 2026 19:04:07 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5557e57c6b69b9c3e5758d5b9d04d5c566d5ed608d90c2811f9b45f584bc9502`  
		Last Modified: Fri, 09 Jan 2026 19:04:01 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355140270cc1b3f0f30a1eadde70d2299bf6f158ca632b51e2c2aa1bb5298f1d`  
		Last Modified: Fri, 09 Jan 2026 19:04:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330c40b41e9259339099f4a391895ec057d142700aeff41316ce5ff25cc5fad6`  
		Last Modified: Fri, 09 Jan 2026 19:08:25 GMT  
		Size: 6.9 MB (6933852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4658c985bb3c8e8ab6ef75c0394d1995da1abb33e5a85ed9b1694a3c7766d08d`  
		Last Modified: Fri, 09 Jan 2026 19:08:25 GMT  
		Size: 92.4 KB (92449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137916fd0b483e71c1ebf6b1d2e20bb375db905e871c540ab152ce54788c9813`  
		Last Modified: Fri, 09 Jan 2026 19:08:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861a34d4e542a1cbc22188269c55dbb3f385bb50dad256d2528283c8b3815978`  
		Last Modified: Fri, 09 Jan 2026 19:08:30 GMT  
		Size: 65.8 MB (65757214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8c040f0ae90a5061a1c44e67cb16fb3377ea04a5f52cf4837620c7303fde33`  
		Last Modified: Fri, 09 Jan 2026 19:08:25 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7694d66e4ef7420a710026b9c98d7e8d998b08e29b559c02958947fb1299d129`  
		Last Modified: Fri, 09 Jan 2026 19:08:19 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:d99bb0c7257b7713bd2da8af434ff0a46a605f5d98fc25a7e999c0dbd247fa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d81f85cd326c95b6d7c87bec23ae759c5c65e988e8fbd2624e828397ffca624`

```dockerfile
```

-	Layers:
	-	`sha256:4300ac3ac0c3a9b26156cf5c0414906005b6cd5fb8cca5188d025c4bae38e365`  
		Last Modified: Fri, 09 Jan 2026 19:08:18 GMT  
		Size: 34.1 KB (34067 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:38ed021920561a9c4d2ae76b0187499465be5b945b8e1c85960cc35421e46f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130280404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53366814e2184be98794066a0c98d79ff7e33eb291353b464e34f149e6193629`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:53:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 20 Jan 2026 18:53:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 20 Jan 2026 18:53:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 20 Jan 2026 18:53:55 GMT
ENV DOCKER_VERSION=29.2.0-rc.2
# Tue, 20 Jan 2026 18:53:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 20 Jan 2026 18:53:55 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 20 Jan 2026 18:53:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 20 Jan 2026 18:53:57 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Tue, 20 Jan 2026 18:53:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 20 Jan 2026 18:53:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 20 Jan 2026 18:53:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 18:53:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 20 Jan 2026 18:53:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 20 Jan 2026 18:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 18:53:59 GMT
CMD ["sh"]
# Tue, 20 Jan 2026 19:09:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 20 Jan 2026 19:09:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 20 Jan 2026 19:09:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 20 Jan 2026 19:09:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 20 Jan 2026 19:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 20 Jan 2026 19:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 20 Jan 2026 19:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:09:47 GMT
VOLUME [/var/lib/docker]
# Tue, 20 Jan 2026 19:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 20 Jan 2026 19:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 20 Jan 2026 19:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea627d0cee44740c67ed3a65085465244cd0a6ce58b0aeb0f663f968d6177f91`  
		Last Modified: Tue, 20 Jan 2026 18:54:13 GMT  
		Size: 8.3 MB (8301055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d280ca8c0ec5863a491d9a7b4af5dda735400331a9da972809d6f8b318ad1dd`  
		Last Modified: Tue, 20 Jan 2026 18:54:05 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47535b6920d2a4c82088ec04ce4e8a60bd55df95e199795e6797208ad1723aab`  
		Last Modified: Tue, 20 Jan 2026 18:54:15 GMT  
		Size: 17.6 MB (17565651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b36b48c567cc1a09c43b823a24effb6c4ff00ee8bb9cd9adfc6f7373d1e84f7`  
		Last Modified: Tue, 20 Jan 2026 18:54:23 GMT  
		Size: 21.5 MB (21476545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31895ed8dd8304cf1a5bd4621a6823e589991222668bcc5f6f7b5ebf10afc4d`  
		Last Modified: Tue, 20 Jan 2026 18:54:13 GMT  
		Size: 10.2 MB (10196866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001e009bee79290e19a8e95a081e4de5466100064f16efead4765e47fc6b2b73`  
		Last Modified: Tue, 20 Jan 2026 18:54:07 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f75f27988de562323c7d3fd3778494f85df268dc319328af9b220db320dc80`  
		Last Modified: Tue, 20 Jan 2026 18:54:12 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906cdddb6979b93b7611875eaeeaf0441dd69b0f50eaa32f404a1c33b0530306`  
		Last Modified: Tue, 20 Jan 2026 18:54:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8af82f811e0c0f7757f2317cf9a2660713f0310be9d4fee2ef2374683c65fb`  
		Last Modified: Tue, 20 Jan 2026 19:10:08 GMT  
		Size: 7.3 MB (7271411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a9363151312eb78e2cb1aed02baa8dfd77b96910dccdf9dd0f2ccf9d531ffa`  
		Last Modified: Tue, 20 Jan 2026 19:09:56 GMT  
		Size: 91.8 KB (91770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4237e4915b31ef97169496a337e85634859d0e7cb514903b93e2b5f44a03b8`  
		Last Modified: Tue, 20 Jan 2026 19:10:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3d12d4773b398eb19e07d96006c6d5c5ff2a6c9ec15559add37f644dd73e92`  
		Last Modified: Tue, 20 Jan 2026 19:09:58 GMT  
		Size: 61.8 MB (61800530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d35efa9a3e75aa1344d9c22be3401d3f6118d70ca824ab15e553c717b9473a`  
		Last Modified: Tue, 20 Jan 2026 19:53:37 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9918b043d932b791022210b38a9be44a21d9f2649c2ec4a58c71f816849d5fb`  
		Last Modified: Tue, 20 Jan 2026 19:09:57 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:efb0856121d942f65aba218b43933f67d28d96062d25ebb915a980d7acea1443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca884723085fd636576634442fe4896af8b01bff331390756df504a09e57e726`

```dockerfile
```

-	Layers:
	-	`sha256:480750beebb028f3d429cb5c0a02a7da40c450e14ec34f9b3ab7d26be40416c9`  
		Last Modified: Tue, 20 Jan 2026 21:07:31 GMT  
		Size: 34.2 KB (34231 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:f34c48465b197cb7718160da968b80094beb246a91960c201f06a57d4007d6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128365887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b870e94c6d431970279ce28560ddebe8fd3b40d924fb28c00bcfe75a0fb88561`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:50:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 20 Jan 2026 18:50:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 20 Jan 2026 18:50:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 20 Jan 2026 18:50:05 GMT
ENV DOCKER_VERSION=29.2.0-rc.2
# Tue, 20 Jan 2026 18:50:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 20 Jan 2026 18:50:05 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 20 Jan 2026 18:50:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 20 Jan 2026 18:50:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Tue, 20 Jan 2026 18:50:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 20 Jan 2026 18:50:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 20 Jan 2026 18:50:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 18:50:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 20 Jan 2026 18:50:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 20 Jan 2026 18:50:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 18:50:09 GMT
CMD ["sh"]
# Tue, 20 Jan 2026 18:54:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 20 Jan 2026 18:54:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 20 Jan 2026 18:54:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 20 Jan 2026 18:54:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 20 Jan 2026 18:54:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 20 Jan 2026 18:54:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 20 Jan 2026 18:54:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 18:54:30 GMT
VOLUME [/var/lib/docker]
# Tue, 20 Jan 2026 18:54:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 20 Jan 2026 18:54:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 20 Jan 2026 18:54:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa74c4bb0952f5ac1cd558e533d42cab2974dec7927c6f1047e8875770599fa7`  
		Last Modified: Tue, 20 Jan 2026 18:50:25 GMT  
		Size: 7.6 MB (7597832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd08f4777a566aae6f9ee174fb4f8f27f48589c741eec0d1c96c61101d682f0`  
		Last Modified: Tue, 20 Jan 2026 18:50:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a6994657451cc62b903ef0afdbb6ddedc32e135e503c5acb63f502fc29b4fe`  
		Last Modified: Tue, 20 Jan 2026 18:50:27 GMT  
		Size: 17.6 MB (17556051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcdc41af803d764df7d2b34a46340dfe9b5177a6d1cf74d0fbc1c341bd4921c`  
		Last Modified: Tue, 20 Jan 2026 21:08:00 GMT  
		Size: 21.5 MB (21454902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233506494f86b5ad8152125430e5b0d777f82b56525323d1c3108a056e397c7c`  
		Last Modified: Tue, 20 Jan 2026 18:50:25 GMT  
		Size: 10.2 MB (10189506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725d884bd716fd9cfa2d38955dd906755dd8ea2937ce378eb1ceccbe1970d1a`  
		Last Modified: Tue, 20 Jan 2026 18:50:17 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e2acd166cd3317fea7004e6b1793842c9294ba62369b9ca8db76db9d7186a`  
		Last Modified: Tue, 20 Jan 2026 18:50:25 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e21074a9b749b400d5b17151ca114cbae831b32e2c4d29232b3498f92721e5`  
		Last Modified: Tue, 20 Jan 2026 18:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c40110a507d05cdd1511574add070b932d90e57806f30238571307486bbdcdd`  
		Last Modified: Tue, 20 Jan 2026 18:54:48 GMT  
		Size: 6.6 MB (6572751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f5008130b2906f398123d4f1b77ea9d22235de01b6f61c7745d5f98eee305`  
		Last Modified: Tue, 20 Jan 2026 18:54:47 GMT  
		Size: 88.1 KB (88127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862e4684cfe1102907b4eff1289a1203be3bd041d0f28b8138b67518c8c1e76`  
		Last Modified: Tue, 20 Jan 2026 20:58:33 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7b6726c54cb8a50c53e1567f8ba2dd71806e2cccb8207ccd5c2acce456c069`  
		Last Modified: Tue, 20 Jan 2026 21:08:06 GMT  
		Size: 61.6 MB (61619181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980fc5a96c5016254ca3264f6428bf191bd46f3ba685015713ea8be3b48cd076`  
		Last Modified: Tue, 20 Jan 2026 18:54:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4ba3384975f5ad73401002bc4c32413b3cfdfe78831bd1c227b952c64e3005`  
		Last Modified: Tue, 20 Jan 2026 20:58:32 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:c5bb11de5f1e00191b6728a9f92ca9b9308b0b3f85f12df7696eb903eb1b3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643de0d8a1ab9cb1dfcf7e9a9a63da2eda0e8af1af75cad37adce6b8b5e4acb4`

```dockerfile
```

-	Layers:
	-	`sha256:5044a524f89fe8a01ef1c1f58b0ae37f58e513c489ded1810b9803b84fc386b8`  
		Last Modified: Tue, 20 Jan 2026 21:07:35 GMT  
		Size: 34.2 KB (34231 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5d317cafe4a63fe232ee4e6b00ca267295a633de23409c0395e7d6dfc3222c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127550556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71024ee4700b79de493c7a0a1c830c8083aaa1e6bca72d390d85538768c2d11d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

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
# Fri, 09 Jan 2026 19:04:19 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Fri, 09 Jan 2026 19:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 09 Jan 2026 19:04:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 09 Jan 2026 19:04:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 09 Jan 2026 19:04:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 09 Jan 2026 19:04:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 09 Jan 2026 19:04:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 09 Jan 2026 19:04:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:04:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 09 Jan 2026 19:04:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 09 Jan 2026 19:04:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:04:20 GMT
CMD ["sh"]
# Fri, 09 Jan 2026 19:08:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 09 Jan 2026 19:08:35 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 09 Jan 2026 19:08:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 09 Jan 2026 19:08:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 09 Jan 2026 19:08:38 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 09 Jan 2026 19:08:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 09 Jan 2026 19:08:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:08:38 GMT
VOLUME [/var/lib/docker]
# Fri, 09 Jan 2026 19:08:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 09 Jan 2026 19:08:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 09 Jan 2026 19:08:38 GMT
CMD []
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
	-	`sha256:ff4d51b3b21450932cee2805a7123133e9f4573a7b11c58cd8b5403f6458a3fb`  
		Last Modified: Fri, 09 Jan 2026 19:04:36 GMT  
		Size: 17.3 MB (17336601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c6e67b130189d9bd8346369da7741d8170a45e5155a2d0cc35b5a50d72c5fd`  
		Last Modified: Fri, 09 Jan 2026 19:04:36 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ef210b183ac9818de60a012961112e58d8d77e6df535f70e0e101217274fbd`  
		Last Modified: Fri, 09 Jan 2026 19:04:35 GMT  
		Size: 9.9 MB (9942175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9e9045bcfa9b4c1745e01cec3aab2e2e326d5177d959c6d981edd741f8aac8`  
		Last Modified: Fri, 09 Jan 2026 19:04:34 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a986189121910f1984ad65d7cab1357e9921b038c672c617641cb81ebe2cfd82`  
		Last Modified: Fri, 09 Jan 2026 19:04:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd48d9cd83aae49267671bb1a05c719a8d4d4f9c4ebb4eba6614a5f4181bc85`  
		Last Modified: Fri, 09 Jan 2026 19:04:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa0671debb5725d86c5b47d3068485134f25d49832c277857c9b0c4d3bec658`  
		Last Modified: Fri, 09 Jan 2026 19:08:56 GMT  
		Size: 7.2 MB (7212657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f120f9f4812efc2f6c570e4de67380b74c73f953228351c8581c687cf2c91c96`  
		Last Modified: Fri, 09 Jan 2026 19:08:56 GMT  
		Size: 101.3 KB (101275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864484020be3347c20db6ccb242f9dddb418a31379ade8b102efc965c948d973`  
		Last Modified: Fri, 09 Jan 2026 19:08:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c65fecd1084ee97a9f9e2304774255baaf1da8c0888c11136c28059f57bca02`  
		Last Modified: Fri, 09 Jan 2026 19:08:49 GMT  
		Size: 59.7 MB (59655402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6711416f796ca5297fb3fcbd58531e2cc01c9bf8657e8a3c635d4a03eda517`  
		Last Modified: Fri, 09 Jan 2026 19:08:49 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1f71aa58a5786ed0c4099abd17e10fdd7f64a2fa5f15620166c296ab0f822`  
		Last Modified: Fri, 09 Jan 2026 19:08:56 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:0a332651cd9105c037f868eb7e75a87beecc76879e41ef1570ed53a26741350f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28be6854a24ef6a6888d567b793dd137d8a8b6bd9bf8cb92b085f233832dcf07`

```dockerfile
```

-	Layers:
	-	`sha256:b2cfb73cba37cbcfe1f6a59602ef162ba2f0fb214ff1c8f7a35fe84374ef828e`  
		Last Modified: Fri, 09 Jan 2026 21:08:00 GMT  
		Size: 34.3 KB (34277 bytes)  
		MIME: application/vnd.in-toto+json
