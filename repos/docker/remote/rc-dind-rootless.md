## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:a7445918a0ff8557fc5651416a3bdc3068fcb036ff199b77f15af244dbe4b6f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9e38edd27ef52dae0be693b73a4df8258dcc70eb7a25927c29c9d7c9d8abe415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158302690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa49fdb28880be48f936d91fc8eb33ed62a601ae333c492e4e3c7eeb43aed1e`
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
# Fri, 09 Jan 2026 20:10:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 09 Jan 2026 20:10:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 09 Jan 2026 20:10:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 09 Jan 2026 20:10:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 09 Jan 2026 20:10:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 09 Jan 2026 20:10:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 09 Jan 2026 20:10:15 GMT
USER rootless
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
	-	`sha256:d1c3502d4e8b80a353244da01568d363e0f0716996556259f33e87fcbc029e6e`  
		Last Modified: Fri, 09 Jan 2026 20:10:40 GMT  
		Size: 3.4 MB (3419928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7831f55a7e564b07f346d77bb758c59a8740af854e641058eccc917f0e2c8af`  
		Last Modified: Fri, 09 Jan 2026 20:10:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd9478207c70a59db6f94f2120ea7ce5bca5712858266223702a2abce04146`  
		Last Modified: Fri, 09 Jan 2026 20:10:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6794428b0e9fb5ca2b81cf7dc6b2f24ed0488783ef33821c407bc276c3cf95`  
		Last Modified: Fri, 09 Jan 2026 20:10:42 GMT  
		Size: 17.4 MB (17371000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30835aee614c71bb04e42b9996137e5158572557272592805b50040eaf42f8e3`  
		Last Modified: Fri, 09 Jan 2026 20:10:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5c4f629fdefb359690058490753de9ed25f129590cb5d9e721177c68b1fac0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ae9d1d7320c59a476a6276acb632f8398109f3d09ea1094febda1001de63d8`

```dockerfile
```

-	Layers:
	-	`sha256:7861dffba9802b338dad8c634b40e6c0fc8281ff4b552e8536c5d9a84866e614`  
		Last Modified: Fri, 09 Jan 2026 21:09:50 GMT  
		Size: 30.3 KB (30340 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fce9428ffd8d98c3324de910b6b130103e74e237da9d9e4f9572b7e211e628fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148655000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7a4fc2053713025e2ee9df00f670305ffb026849c5e8ade7eba8f11cd4bdbb`
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
# Fri, 09 Jan 2026 20:10:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 09 Jan 2026 20:10:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 09 Jan 2026 20:10:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 09 Jan 2026 20:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 09 Jan 2026 20:10:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 09 Jan 2026 20:10:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 09 Jan 2026 20:10:13 GMT
USER rootless
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
	-	`sha256:2a59a39a3a23555ab3591b9f670f9d7bc4d46203ef8a5f3f7d47076839087498`  
		Last Modified: Fri, 09 Jan 2026 20:10:20 GMT  
		Size: 3.4 MB (3394357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d25dd88fe11b31a45eca174f28ddff2d8ebc82d169a16fc71da8ccdc4218f56`  
		Last Modified: Fri, 09 Jan 2026 20:10:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6899a636d4bb1e19a2423b7d94735c231252d217be4a88679cdaa96b34188b3f`  
		Last Modified: Fri, 09 Jan 2026 20:10:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d980c9e6a596476259c05b2970bdb9339b6cf123571a5960db89cf1e478c77`  
		Last Modified: Fri, 09 Jan 2026 20:10:39 GMT  
		Size: 17.7 MB (17708747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee176ff08b30214d42f648a51c9bc1a1b0fd0e37c97bc99d427c7ab65224e06`  
		Last Modified: Fri, 09 Jan 2026 20:10:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ce3c2902582bb482c46a670e7dd360f00c24ff044412d2fb0b4fb9b9b388aea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f95432cfde3fcf4842eb9651923482e4c53a4cd0a7dbbb04867eb48561a701`

```dockerfile
```

-	Layers:
	-	`sha256:97ba8ad08f2482d97e694630ff414e5e4f39043f268cd7dedae9c3baa25c387e`  
		Last Modified: Fri, 09 Jan 2026 21:09:54 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json
