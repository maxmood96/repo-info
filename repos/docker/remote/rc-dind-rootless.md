## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:cb9c7a7df35a40c794e26cd53933b243dbf4f905a4c4641a4220600df64d6167
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

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

### `docker:rc-dind-rootless` - unknown; unknown

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

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e74a5cae74c830600c04eabb1b1a348c597fa4a427326de3e7afada81f53a894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160921060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478a02e2ff19899673ecc841cffd01dc68b5c0467920c483b72c576928e786b4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 17:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
ENV DOCKER_VERSION=28.5.0-rc.1
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 25 Sep 2025 17:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 17:04:22 GMT
CMD ["sh"]
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
VOLUME [/var/lib/docker]
# Thu, 25 Sep 2025 17:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 25 Sep 2025 17:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 25 Sep 2025 17:04:22 GMT
CMD []
# Thu, 25 Sep 2025 17:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 25 Sep 2025 17:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 25 Sep 2025 17:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Sat, 11 Oct 2025 10:00:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159de46bb8b0ef6398fe2497ebe83a93e3ecf7a2f72014fcdf50dfe4f653e39`  
		Last Modified: Thu, 25 Sep 2025 20:53:59 GMT  
		Size: 8.2 MB (8216529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b346d0d6accdd625288f88291917533d9b785a0d785dca8ad2a6b70eb55bfcc7`  
		Last Modified: Thu, 25 Sep 2025 20:53:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c69e340896eace13b37482a31074b4c89fe5a2f4b6f5d3e93e9b9dd75d6ea`  
		Last Modified: Thu, 25 Sep 2025 20:53:59 GMT  
		Size: 19.2 MB (19239526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99054b3b90bc2c3b00e376895fc849779ae26169f8b98958dcd60fa33cac991`  
		Last Modified: Thu, 25 Sep 2025 20:54:00 GMT  
		Size: 20.2 MB (20248424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4225a676b4e5e72a59e8bc2eb92b4308754f1b2c736d5db3fe43079379894624`  
		Last Modified: Thu, 25 Sep 2025 20:54:04 GMT  
		Size: 19.8 MB (19779979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b8d626449b544a95678f7375ad200a98148de1d8354955ee26f3ca4d4d381`  
		Last Modified: Thu, 25 Sep 2025 20:53:58 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89f9c375f8837b1876dbbf151fe6213c75b79f0b77ba985904f569cee58a030`  
		Last Modified: Thu, 25 Sep 2025 20:53:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efe8b28852a4fe4e833418ef0ff833fa69888cb0bc7c2e492f467138f3b9cd2`  
		Last Modified: Thu, 25 Sep 2025 20:53:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ec06b555565a99aca32ca52fbeb5e429d2871a7d805775e58776a86dd7f552`  
		Last Modified: Thu, 25 Sep 2025 21:09:01 GMT  
		Size: 10.0 MB (10031909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd95283aa8210d5f4109569e55f1c48b60536feb269ac74c16be325f4cce7dd9`  
		Last Modified: Thu, 25 Sep 2025 21:09:01 GMT  
		Size: 99.3 KB (99309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c65cfa7ca2c263920702c0a5c64216d846410c0694dab48849f1c64c4a239dc`  
		Last Modified: Thu, 25 Sep 2025 21:09:01 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b30aaf1c63e1f4548d05b16568479766c46fde8f8dbd0e9abe901797bfc95`  
		Last Modified: Thu, 25 Sep 2025 21:09:12 GMT  
		Size: 57.8 MB (57755706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f1d2022504e149f3dceb3638ce540ec0fe232487a134f90cb3eb2cfc5a79a`  
		Last Modified: Thu, 25 Sep 2025 21:09:01 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8664850e66258055290d89317f73decf0339522060cdaebeff1da82cde59e2`  
		Last Modified: Thu, 25 Sep 2025 21:09:01 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb3e02d99db0c60a7bef0887b7bc39101a00da6d9462d44ebf55fb57b0b831b`  
		Last Modified: Thu, 25 Sep 2025 21:12:07 GMT  
		Size: 3.4 MB (3390000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5393ab03087643e0ac640a9f2ad628f1612040983efcd1c089c0f8868aff2`  
		Last Modified: Thu, 25 Sep 2025 21:12:07 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea362fc7fc406c0100c692174d30a6271f58c5ffd76eeea288651f287954b801`  
		Last Modified: Thu, 25 Sep 2025 21:12:07 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1bbe086470136075b5af8ea5035fc033c97cb77ce4baec588c114cbef4545`  
		Last Modified: Thu, 25 Sep 2025 21:12:08 GMT  
		Size: 18.0 MB (18019431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64e153fab41db7ead526d303df0ebb7362bc97b5720240284772688c1318e4d`  
		Last Modified: Thu, 25 Sep 2025 21:12:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f99a16b26445b45e02078229f910f40ab3aeb08d89313d961d2d149a04eec235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a48d639a2c4a67f956b16adc88fbe02c9fe081a9afb44ddcf350eb6a90e1dc`

```dockerfile
```

-	Layers:
	-	`sha256:5ed25c7429c60b33163ab217fbb7c05adad6408f60a1426e7f9385aed0789dbe`  
		Last Modified: Thu, 25 Sep 2025 23:08:50 GMT  
		Size: 30.5 KB (30544 bytes)  
		MIME: application/vnd.in-toto+json
