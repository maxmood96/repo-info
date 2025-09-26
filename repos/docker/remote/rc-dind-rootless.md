## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:ff973b41aed2f2813cca4f16e7dd277d6cdf75c94ba58227a3c7d7ed8c860abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b830ceee59a25d2c95bf647ac291c46ef06e2fd5e0c787807235cd10750ab535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169636159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163f1ff5dd2b8831f2cc0c05470f63dc2221ff708b771b04bb47117942026b7b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c811d3a0ce628e18cd2102f41b09a12de94aff3009128adedaf8be05ccb652`  
		Last Modified: Thu, 25 Sep 2025 20:54:08 GMT  
		Size: 8.2 MB (8198691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e68de1e1b66fd3935b7a551b53e81eb4fa56da7ff46bb1cf59fbd3b730fcee`  
		Last Modified: Thu, 25 Sep 2025 20:54:02 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a9d7a682203511de8979d7cc942374955ffd68d9ac9cef8c41132134252c6`  
		Last Modified: Thu, 25 Sep 2025 20:54:14 GMT  
		Size: 20.4 MB (20430958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b15d70b14e347712afee542e259cee02dabe811cded018ad06ecc81d61e732`  
		Last Modified: Thu, 25 Sep 2025 20:54:15 GMT  
		Size: 22.1 MB (22129665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4649484746a1931490526bf413a95c0cab154a80618f7687e178cdcbd32fd845`  
		Last Modified: Thu, 25 Sep 2025 20:54:06 GMT  
		Size: 21.7 MB (21656778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee72110cacf34c8ab9187aa61b9b8dff334dc8050aa147b9013c3dfe815ab2d`  
		Last Modified: Thu, 25 Sep 2025 20:54:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf2a000030ff3d46dc6eb7aa7d3578c678e5705858b73e60b9e098022ed3836`  
		Last Modified: Thu, 25 Sep 2025 20:53:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efe8b28852a4fe4e833418ef0ff833fa69888cb0bc7c2e492f467138f3b9cd2`  
		Last Modified: Thu, 25 Sep 2025 20:53:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd631ba2c38d5847de591569b93f6209d675b3fab315b5a3a2128dbf5d213d`  
		Last Modified: Thu, 25 Sep 2025 21:09:14 GMT  
		Size: 9.5 MB (9502639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720c804965ed7970a285db0d2a3de270ae46bc2f1624651a946393f7b699caed`  
		Last Modified: Thu, 25 Sep 2025 21:09:13 GMT  
		Size: 90.2 KB (90238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3788d1dc23fb9c16a0fc29a737897cd49977d7ac8f6c0a7b4c7440d90988df59`  
		Last Modified: Thu, 25 Sep 2025 21:09:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4459d08e73f82cc68c2585b71cac580067835656251ea41558a0f31973fbaddf`  
		Last Modified: Thu, 25 Sep 2025 21:09:21 GMT  
		Size: 62.8 MB (62827527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd808c4f8b47118e7529a7a300e87bac0d6901100a856df39e5ab6deb49d87`  
		Last Modified: Thu, 25 Sep 2025 21:09:14 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06d5eb78fb7c77108ecb89f640e0dd8bd58ea25ced5ec7ac1973463f5c774cc`  
		Last Modified: Thu, 25 Sep 2025 21:09:14 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7fccc0834d8f58a9d3a4e1693d4b1e2b44ad06c9e83ef3b189f0caf94a381a`  
		Last Modified: Thu, 25 Sep 2025 21:12:57 GMT  
		Size: 3.4 MB (3398479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6109717d1278f917953e677dd85c2740ac62c8b55fd1ef6d540ca6d2900c`  
		Last Modified: Thu, 25 Sep 2025 21:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7f0feecbd14cf0ac3f459d1db49fc7e2c7e3f8a21a8ec08427aef8b6103a3`  
		Last Modified: Thu, 25 Sep 2025 21:12:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3961ab55e1a93d5a721263fec64f512183001da8aaeb5de4c463dbf694222a`  
		Last Modified: Thu, 25 Sep 2025 21:12:58 GMT  
		Size: 17.6 MB (17592012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a4a06875ac286469a02215845be6ad6ada0f1d54c63c497b860f5269032cf`  
		Last Modified: Thu, 25 Sep 2025 21:12:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:dafb83d4f0699b503db0a44743a6622a37e86327e5e1a7a5538378e81a52608b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d02a76d84e71ba82e6d4a30103f6a6638934ccf5df2e2bcda024ed5758d58b`

```dockerfile
```

-	Layers:
	-	`sha256:fafb88e50e09773ba51135762fd6e8055b237f21653f75a67289f582bce73821`  
		Last Modified: Thu, 25 Sep 2025 23:08:47 GMT  
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
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159de46bb8b0ef6398fe2497ebe83a93e3ecf7a2f72014fcdf50dfe4f653e39`  
		Last Modified: Thu, 25 Sep 2025 20:53:59 GMT  
		Size: 8.2 MB (8216529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
