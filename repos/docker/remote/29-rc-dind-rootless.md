## `docker:29-rc-dind-rootless`

```console
$ docker pull docker@sha256:18008e64b433f8c0947e74175909454bc40c14ab4f8f047d9a7b92d40d3b9ef9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a2427d8002edd2b4c88858e864d5db216c6b06ad24a29aaf3ba4362496f624d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166470153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901eeb75114e741253b93f010e305513697a327fa7b614f1132debf13ef0bb12`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 14 Oct 2025 15:11:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
CMD ["sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
VOLUME [/var/lib/docker]
# Tue, 14 Oct 2025 15:11:51 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 14 Oct 2025 15:11:51 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
CMD []
# Tue, 14 Oct 2025 15:11:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 14 Oct 2025 15:11:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bbca4dac63dda61c15f026e41128ceed724306ef1926d3af5d649611f35255`  
		Last Modified: Tue, 14 Oct 2025 18:16:12 GMT  
		Size: 8.2 MB (8205949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5cd71a5c62247f7db914287661a8deb65e131718c0084f0d71f362ef99d296`  
		Last Modified: Tue, 14 Oct 2025 18:16:10 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3005f77ab24b95f065333d3986387a41de710df6d63d9bee7955e0e8b0d08a`  
		Last Modified: Tue, 14 Oct 2025 18:16:14 GMT  
		Size: 19.7 MB (19747043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aa0124a3341a72d24da8293b5701732bf7eab02a8e49d385a7fd7e13d9a519`  
		Last Modified: Tue, 14 Oct 2025 18:16:13 GMT  
		Size: 22.2 MB (22158448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067eb0191e16ecf0c10ad1e1131b6a544e172f6924eb7265c34715c3e05dd165`  
		Last Modified: Tue, 14 Oct 2025 18:16:15 GMT  
		Size: 21.6 MB (21626192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584b85e33c6ec61753c205e4cb367af564cd72d841fb5760898fe64a32122dbf`  
		Last Modified: Tue, 14 Oct 2025 18:16:11 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6307e1d8df66aa28d2bfcd0f6b190d5f812d3c4611bc69cc54e6a5c4e51be4cc`  
		Last Modified: Tue, 14 Oct 2025 18:16:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e1e2cbeac74f1006714d0ff16cf9f940746e7899999bc940e66c1d417eacb`  
		Last Modified: Tue, 14 Oct 2025 18:16:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54af9b50860a53846b419e9b761197ecb1c02edb6105dfda14592a2788b68315`  
		Last Modified: Tue, 14 Oct 2025 18:56:12 GMT  
		Size: 6.9 MB (6905422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fe6d5a53fb7468210bd3fdf94ea034518a3e40c9b1462acae036111e4946dd`  
		Last Modified: Tue, 14 Oct 2025 18:56:12 GMT  
		Size: 90.4 KB (90384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81d6966c0ce01d484069f122810ed75834a876722ed3ccb1a7d0f00f899774`  
		Last Modified: Tue, 14 Oct 2025 18:56:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8761c727faf1400c03d2198ecc581ecc347303dd0dd7503046fb4e94a50fe121`  
		Last Modified: Tue, 14 Oct 2025 18:56:19 GMT  
		Size: 63.2 MB (63156166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c594061183ce2ee5a2505c08150b0c0e164ccd40bbb148d174cd5322cc63e5`  
		Last Modified: Tue, 14 Oct 2025 18:56:11 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49cba3c4dfdced4bd5f7fbd1d6c094846723ab69fcbdc544baba52460c8c901`  
		Last Modified: Tue, 14 Oct 2025 18:56:12 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbbd0e8e9354977820e6618c84ab271431ab08d07256285405f838a3551c48b`  
		Last Modified: Tue, 14 Oct 2025 19:12:11 GMT  
		Size: 3.4 MB (3398367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bec655fe2c92d4191f0819e9e116c41d965a7c3ff867672670e39aa63e0d216`  
		Last Modified: Tue, 14 Oct 2025 19:12:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fad1c148034c37378990a66bd191b7a53636b427c9f32fb0ebaa32fa5341476`  
		Last Modified: Tue, 14 Oct 2025 19:12:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271f3009921894aa101a8e8174f558e1a62a728ea5e6638f7e2b74b06b3dc506`  
		Last Modified: Tue, 14 Oct 2025 19:12:12 GMT  
		Size: 17.4 MB (17370233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7628f71203040b1170f9660ae753579549382d8ef3bddf59b535d78247ee16e8`  
		Last Modified: Tue, 14 Oct 2025 19:12:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bfad24571276b898b0dea09b068bdf5865cb2505e4a4a31db39c8bb41d38b2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fef67f35b3ceb96af87cc8212c2a73be5a3ea8ee9ec961c21961274774a825f`

```dockerfile
```

-	Layers:
	-	`sha256:db345f113c66fbe8d9f3a555bb1172d93eb6e47bc802302faf694d8fb383d6e8`  
		Last Modified: Tue, 14 Oct 2025 20:08:57 GMT  
		Size: 30.4 KB (30389 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e7d04fcb2f899d92298c5c103fd2c29a61d43bf50566047bd7cc4a1313b78ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156299331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8742ef3cca45aa0472dadedcd4575f9dc9092c4cac8dd700f0d4673471c02170`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 14 Oct 2025 15:11:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
CMD ["sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
VOLUME [/var/lib/docker]
# Tue, 14 Oct 2025 15:11:51 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 14 Oct 2025 15:11:51 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 14 Oct 2025 15:11:51 GMT
CMD []
# Tue, 14 Oct 2025 15:11:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 14 Oct 2025 15:11:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 14 Oct 2025 15:11:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b10e0305b1e19fc16fd80eba3c72fc942b09acfdcc0d3540a4e16902fb22952`  
		Last Modified: Tue, 14 Oct 2025 18:17:30 GMT  
		Size: 8.2 MB (8227549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abbe9e2de40ec4b6ec5d0ddaae54a61ccea7854a8e6083ba1896eb1f87c9934`  
		Last Modified: Tue, 14 Oct 2025 18:17:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01990adf97c0b40d144de38838718ee85c7aad6900c0536896ccf67f05fad2af`  
		Last Modified: Tue, 14 Oct 2025 18:17:31 GMT  
		Size: 18.3 MB (18256393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8d87c8051c8128007e5b8de599dae3fdaa21d825458d872a4b7a0aa7a115b3`  
		Last Modified: Tue, 14 Oct 2025 18:17:30 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18e52451505b7e8d643b576eddae489e9f0447778788422e0be149aaa942cc6`  
		Last Modified: Tue, 14 Oct 2025 18:17:31 GMT  
		Size: 19.8 MB (19755377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6de01507dcde6cc0ad11b4896bd257182b39f0922178cb57f4005be5da3b47`  
		Last Modified: Tue, 14 Oct 2025 18:17:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef632edb75087d839168a9728b8c43422e80e0479f1f95ebd396634e6b6a738`  
		Last Modified: Tue, 14 Oct 2025 18:17:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87dda9dfa6953b97784730f4d512e3afcc6001d0e4875e12b3af4d910957114`  
		Last Modified: Tue, 14 Oct 2025 18:17:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5dd0092c48e973dba7db4b5558acf9d6586151af0b4ee2b88f82a427ba6d0e`  
		Last Modified: Tue, 14 Oct 2025 18:54:30 GMT  
		Size: 7.1 MB (7140760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e659cdefc6c6a5277923b80ba50499fd36ea1f3c1e2d07d5e83709d4c45660`  
		Last Modified: Tue, 14 Oct 2025 18:54:29 GMT  
		Size: 99.5 KB (99504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1640d4c1164e3630f65efa560ac18d70ba83af4d0e53028ffc17e96bf6a4a0`  
		Last Modified: Tue, 14 Oct 2025 18:54:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe58fbf9ba9ac959e3924f2628363165b3cf919b5ffa6dda937f114da50fab5`  
		Last Modified: Tue, 14 Oct 2025 18:54:35 GMT  
		Size: 57.3 MB (57302053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0c60160018464de53400bdc9f2a90eaf48c66f75f89ffdad84bdb731318090`  
		Last Modified: Tue, 14 Oct 2025 18:54:29 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2159f863798117f05d4b39bfb8a62961d4baf5ba9d707767b8e3d6ceac5ba9a3`  
		Last Modified: Tue, 14 Oct 2025 18:54:29 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d3a40ac707977e56732db12d1c6b8775962c81e01a48d214132dcc7fb6e31d`  
		Last Modified: Tue, 14 Oct 2025 19:09:27 GMT  
		Size: 3.4 MB (3389913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a397a098b2ed76cf7a8756ab6f8f5280c766518a55c831bb13f7006bfeed10`  
		Last Modified: Tue, 14 Oct 2025 19:09:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069b73c2948c0a0877c35be843544f1e46f3be899d2ea4cd1f241d2ae508163`  
		Last Modified: Tue, 14 Oct 2025 19:09:26 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b8d06a772731e4ca08e91b9106a4b2288f7bad5a40a23c19a7f65b018d4a84`  
		Last Modified: Tue, 14 Oct 2025 19:09:29 GMT  
		Size: 17.7 MB (17706813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadaffb73b9acf736ed8f391e233356c972592ba7094a5ce8b9023f5be71042d`  
		Last Modified: Tue, 14 Oct 2025 19:09:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2d447f1de25b3c176fbb34f043d8a61916da4804a52b7904bbb95499b2167046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1492fe4344734d3389e9fa9271cf606ced07e2cd0863dad3eeb3015929dd2205`

```dockerfile
```

-	Layers:
	-	`sha256:d22f0a20304682c34bc48bb4845c46d48485b30916093ea3d9fefdb25cdd6931`  
		Last Modified: Tue, 14 Oct 2025 23:07:57 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json
