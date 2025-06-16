## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:70f2e3be8e1233cd23dc847bb0235333964dca22b6e26971cbd610d27dd67cba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e45baad914554a011c55b99da64d8f11ec17aa0987c3417ead7a69c7f86bd581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161745542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a4a37901d1a651641bd975a6c6aba89091ccf312070db108af0c5f8e515f90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 23:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DOCKER_VERSION=28.2.0-rc.2
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 23:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 23:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 23:04:23 GMT
CMD ["sh"]
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 May 2025 23:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 23:04:23 GMT
VOLUME [/var/lib/docker]
# Fri, 23 May 2025 23:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 May 2025 23:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 May 2025 23:04:23 GMT
CMD []
# Fri, 23 May 2025 23:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 23 May 2025 23:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 23 May 2025 23:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969c3d2d17956de43f5c8af3d9249b03c4059a89206f2f1cc5ba1dcd0a23901c`  
		Last Modified: Tue, 03 Jun 2025 14:26:01 GMT  
		Size: 8.1 MB (8062901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31464bee96db3ab49cff71c7c1e3d953b9387b7b3fe8988e6de37da9a605f0f9`  
		Last Modified: Tue, 03 Jun 2025 14:26:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979da331a0d1a4262e9c51b0398244c954d559c6a0e40f4b7ace935ba0237490`  
		Last Modified: Tue, 03 Jun 2025 14:26:04 GMT  
		Size: 20.1 MB (20081539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2073afae2626cf5680027be99753f0407257de6381abb1daef12428eef3040`  
		Last Modified: Tue, 03 Jun 2025 14:26:06 GMT  
		Size: 21.3 MB (21290153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8f5f0100ec48090a0a3023ee086e76c9873a3e6b78cfde4309d4947dc2729a`  
		Last Modified: Tue, 03 Jun 2025 14:26:09 GMT  
		Size: 21.1 MB (21083725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f812b6d4e0b7b04a0e455709d11a28f92a7767e49fdf93e375a565d1e19b5964`  
		Last Modified: Tue, 03 Jun 2025 14:26:09 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3087dafa23644ba5e9fea25d334fd6c984e4ebe610296a36c987e10dc9f4bf`  
		Last Modified: Tue, 03 Jun 2025 14:26:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc1f20e6764b41722068b4374406904ae8c265b57cc905ac66de5854211574`  
		Last Modified: Tue, 03 Jun 2025 14:26:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aab42277c861271b024b3ea1f07ef5cffda004989cc80675d71725cbb6f1f16`  
		Last Modified: Tue, 03 Jun 2025 14:26:13 GMT  
		Size: 6.7 MB (6732948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9056ffff85c7d17095e6494a75f3b04bf9cad52ae8aea20cff30c507189a69d`  
		Last Modified: Tue, 03 Jun 2025 14:26:14 GMT  
		Size: 90.3 KB (90339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6aa99fa3d34505cd0906d335ce7dc8e9a0421c30cbe0b2d210ca54f34515a8`  
		Last Modified: Tue, 03 Jun 2025 14:26:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28743aaff67d69db637e786c68eea203c5319c482de4ac398892d1cb022c05e3`  
		Last Modified: Tue, 03 Jun 2025 14:26:20 GMT  
		Size: 62.2 MB (62179637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5758752eb77c877e7b65a6473b4fca9c23017c75e23cf76a7a7e5c2da252f48d`  
		Last Modified: Tue, 03 Jun 2025 14:26:20 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8f0c1ca01397a1218a79d83621bbafecf8de80a9707b129dc7a17dea42312b`  
		Last Modified: Tue, 03 Jun 2025 14:26:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9016eff4b65f8ba2be2d96a23a02f14ac2021d096135e0b636264c4ffa0742`  
		Last Modified: Tue, 03 Jun 2025 14:26:22 GMT  
		Size: 986.6 KB (986585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49ffacfa54c23ebbe556a337655fe2633b10455bfa48a0088249ec7f20c3834`  
		Last Modified: Tue, 03 Jun 2025 14:26:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d2c32d0295f05897b031f40a4737be4433c7490afc1671a2bab1f241253a73`  
		Last Modified: Tue, 03 Jun 2025 14:26:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fc597b700d97b4a9adaac0afcdd7375fe89b69925f3631f089387c762e3b6f`  
		Last Modified: Tue, 03 Jun 2025 14:26:26 GMT  
		Size: 17.6 MB (17585977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4637f46bd2a0ce873dcc4c24398f6f19e33511772fe8d19e73802d7dddf5bbd7`  
		Last Modified: Tue, 03 Jun 2025 14:26:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:140d6433fa6d680541786294702779c77a6de96cf1beb24c3bc8d2f8ec683844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d35d35ce228e429ee67afc8f4beadbea91a7c9eaff94fe0bad14270e9797ff`

```dockerfile
```

-	Layers:
	-	`sha256:b11f8f3b0d36047ae81bdfdd3e54bf64a1fef3c57e4dca8e9da298dd0e6515c5`  
		Last Modified: Tue, 03 Jun 2025 14:26:30 GMT  
		Size: 30.2 KB (30204 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:891fd56ff126fab2c128ccf169d8c3acc2c9451adbc975a32b2c6d47938f2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153021255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96fc9fb1732cf9ec560f1866c5e67149a99d149d77dad1bca45712f63826e91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 23:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DOCKER_VERSION=28.2.0-rc.2
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 23:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 23:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 23:04:23 GMT
CMD ["sh"]
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 May 2025 23:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 23:04:23 GMT
VOLUME [/var/lib/docker]
# Fri, 23 May 2025 23:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 May 2025 23:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 May 2025 23:04:23 GMT
CMD []
# Fri, 23 May 2025 23:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.2.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.2.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 23 May 2025 23:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 23 May 2025 23:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 23 May 2025 23:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e61ef9ca0a32b5626ac08a081ee2fb285c4ba038cf94557ba2bef2fb41c4ec8`  
		Last Modified: Tue, 03 Jun 2025 13:42:05 GMT  
		Size: 8.1 MB (8077214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b23db6bcf28bd3ae33e7be5a3fbb71d9a7198495c73d38a13ae6982557374b2`  
		Last Modified: Tue, 03 Jun 2025 13:42:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cf776735acde2c2b7c18bf1b619b6ab1cbb1a125b246ac1922d667452dda0a`  
		Last Modified: Tue, 03 Jun 2025 13:42:06 GMT  
		Size: 18.9 MB (18903227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b683d68961e1651a25f1996aa3b6691db85ac4cb32e97ba929e519e8f19f2`  
		Last Modified: Tue, 03 Jun 2025 13:42:10 GMT  
		Size: 19.5 MB (19469842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6ab2ba05b0c49cabb7ca88e83ca7b7e946f1d427fd430c3c1340bd169e17`  
		Last Modified: Tue, 03 Jun 2025 13:42:13 GMT  
		Size: 19.3 MB (19324581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e8cc53c75c603182a435767d43032199d0d14457ef3aa06844b09d5685c85b`  
		Last Modified: Tue, 03 Jun 2025 13:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b717a2e022e70ec17ab5b0722c458f01f12ea59c12213fe7d169d9e5a13daea5`  
		Last Modified: Tue, 03 Jun 2025 13:42:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef43143375348182679dd308c49859edf0ba35b2782aaf824ebb0d01715c8d4`  
		Last Modified: Tue, 03 Jun 2025 13:42:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e9897f1db458590e77dd15dbe8979ef67fee439636805c194da34015c40437`  
		Last Modified: Tue, 03 Jun 2025 13:42:17 GMT  
		Size: 7.0 MB (6978901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ed810840a4fa592f947f2213ba2e562292b06e6baa7725d6a8ca43d7e4939e`  
		Last Modified: Tue, 03 Jun 2025 13:42:16 GMT  
		Size: 99.4 KB (99402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8d778e8001f82dbd4a4f1436b682e5558fc44c212b6c2c6c8aa35a32b80aa1`  
		Last Modified: Tue, 03 Jun 2025 13:42:17 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d57bd19addb6911a44b5ec6f13c8aeebeecf667e9826cb83077fe41607490d1`  
		Last Modified: Tue, 03 Jun 2025 13:42:24 GMT  
		Size: 57.1 MB (57135162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754652e3c0d1a2f592f20416c3b0251e58ae9e4128ca337339ffb15de36e3b8a`  
		Last Modified: Tue, 03 Jun 2025 13:42:19 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dee82e52f84e01ec06805b5f24eabb84d5f7088380d01caedf4d4255a741`  
		Last Modified: Tue, 03 Jun 2025 13:42:20 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f95ba8242f84f71d937edd75078e2ce26c9caccfbcf92f4a33884014ddae5`  
		Last Modified: Tue, 03 Jun 2025 14:26:55 GMT  
		Size: 1.0 MB (1014218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db98bc2f2336ed38389f2889bf25c585c006c60826d32870cd43122f631e8752`  
		Last Modified: Tue, 03 Jun 2025 14:26:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7835008dc50bf2fc8ddfba1fffd615c5266a9201f08f1e7da322fbbbec67b7a`  
		Last Modified: Tue, 03 Jun 2025 14:26:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657a977086a5fe1ecf20f8f6b3df34d0718261e25b707399b9358f42e857247`  
		Last Modified: Tue, 03 Jun 2025 14:26:59 GMT  
		Size: 18.0 MB (18016187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e1391970484ff23730db136649e2542d61f624ffb922839620e272d00b5973`  
		Last Modified: Tue, 03 Jun 2025 14:26:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:16600ae68993e399e2808d5bffcf5ed1d772c7c85352762e036962b6a94db31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ca6aa9f966a8b8ce0c54584d4d93020debd3b2a6870ead059a73964fb8fe96`

```dockerfile
```

-	Layers:
	-	`sha256:e0237c923c3e69c82898c0f040b804077fd0ca64e3c4ebb046b153aed98e2219`  
		Last Modified: Tue, 03 Jun 2025 14:27:02 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json
