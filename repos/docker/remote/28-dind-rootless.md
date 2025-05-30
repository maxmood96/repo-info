## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:69d0d22b76699f0e1a25b983290b176121550f6563adcff0fa86b9ea2ffacae1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a4f2ebcfc1373ea8574f9c5200c53f98a7b0bec2918e8cd6b75e6df1e99d4df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161754123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb58e5cce97e2061455675d11a443ee776255c3b3ccd50217308675c20113a0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 23:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DOCKER_VERSION=28.2.1
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 May 2025 23:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 May 2025 23:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 23:04:17 GMT
CMD ["sh"]
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 May 2025 23:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 23:04:17 GMT
VOLUME [/var/lib/docker]
# Wed, 28 May 2025 23:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 May 2025 23:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 May 2025 23:04:17 GMT
CMD []
# Wed, 28 May 2025 23:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 May 2025 23:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 May 2025 23:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2c9272a8e1c405812f53f7f40e62801a89f346ef38365b8549f251bf8a0c24`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 8.1 MB (8062887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d66dea1dd50fda031a4f3847763a299ee227335b6d6ea9fa7aff9915e9cbb`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ba8513ca5a53f5f4748c9799733be5fe9abc57ddcea9aa14875c3e49bfaeae`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b9bab656542ddf27b8e91b080822d8ad4682218cea01718f5bfa397e2c3c84`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 21.3 MB (21290165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248a6b0cda0c133abb137ed8a3ec86dbc9430ded559fe2c7d5eb1bc66fa1e4c`  
		Last Modified: Thu, 29 May 2025 21:13:28 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae39727fc67375c841550a6b8be9c2aba13799a5a3803b5bb81e4e5e13629d7`  
		Last Modified: Thu, 29 May 2025 21:13:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ce9bdf07d9112a6d62b7e9ad6905183f231ed775474c323a088b19936c1acf`  
		Last Modified: Thu, 29 May 2025 21:13:28 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8759ef612a5e036abfa1561905859b6b3fc14d9a58659eb2a619ac4a8da9783`  
		Last Modified: Thu, 29 May 2025 21:13:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4eb3fb46f3d4a5c9053d290588249a37df86678ff04379c1761556d93dadc8`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 6.7 MB (6732956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7012a197b205414c3954dd8585a653abaae6862b92e7e0cda9bea7b2e4ac7ce8`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 90.3 KB (90333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5740925ba2456d58bc24797ab298cb4dc1f6a294f7a70a5ff3ae9cdb2c8ce6c`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cd3be09272a282c8114654ed57a350d4dfee798c7374bb391550bd4c348661`  
		Last Modified: Thu, 29 May 2025 22:07:47 GMT  
		Size: 62.2 MB (62186737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04395ce8ed2dd59659f18937d3f215720df1d13a455565aa02c3c3c25e84879e`  
		Last Modified: Thu, 29 May 2025 22:07:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baabbe011ddc93dced76fdfec1443be719aa26239101f78f98ebd01292f031c0`  
		Last Modified: Thu, 29 May 2025 22:07:47 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3b6941473a413c0ecaedbd977779b8f4ebc6a37f720242d1c1f127586d6ccc`  
		Last Modified: Thu, 29 May 2025 22:27:53 GMT  
		Size: 986.6 KB (986585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da4ab0ec4a9371e9562c6f4195f21f476d21574a71e78c8f3b58f4f711924f9`  
		Last Modified: Thu, 29 May 2025 22:27:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fbb2022dc5a95a4fbca8ab8164a878c3459dffcc7305ec98e24ec2f929dc9b`  
		Last Modified: Thu, 29 May 2025 22:27:53 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ae6931ef155c81aefb2de9b7a85e424541ba32fe87514bcdec2127584a16ad`  
		Last Modified: Thu, 29 May 2025 22:27:53 GMT  
		Size: 17.6 MB (17585957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438842273cf596a51e0025a8d8bd81f5b71d4af1a06fe7e11e2091f27f8db50c`  
		Last Modified: Thu, 29 May 2025 22:27:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5dfc3bff48b1fa577f07802099b766491ecef25c96e970b78a433a9fb899ba16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31063f7190149751d42cbb50e5a9986f1a95bb3c9e5025e45b0eb695be134608`

```dockerfile
```

-	Layers:
	-	`sha256:36eec28b378d142610f0d9d27ed5306ade215b32683256655a4d75a591b6878c`  
		Last Modified: Thu, 29 May 2025 22:27:52 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:046925f0ce93d00144d85bc45c93bb44f0405627429cd488dcd0a25a6f35c511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153037620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d5ff0ce3982cb1a1bf49f0a31095e95d04f94b359f0792d867b0427eabb2cf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 23:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DOCKER_VERSION=28.2.1
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 May 2025 23:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 May 2025 23:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 23:04:17 GMT
CMD ["sh"]
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 May 2025 23:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 23:04:17 GMT
VOLUME [/var/lib/docker]
# Wed, 28 May 2025 23:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 May 2025 23:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 May 2025 23:04:17 GMT
CMD []
# Wed, 28 May 2025 23:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 May 2025 23:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 May 2025 23:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 May 2025 23:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167ada91b6e7d7f8f290c8fdea25205d6ad64d4c395e243e9b1f59e4af63f043`  
		Last Modified: Thu, 29 May 2025 21:20:56 GMT  
		Size: 8.1 MB (8077224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c326ddc7f7db2a73aa3bfd66f3f9fd394d3207682679f182598ca6e57f9700`  
		Last Modified: Thu, 29 May 2025 21:20:56 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d770584d351075d0aa0692a00c074495ec6c42bfa477a2757d5537b9c447d7`  
		Last Modified: Thu, 29 May 2025 21:20:57 GMT  
		Size: 18.9 MB (18902602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59c930e3148dfe9cbc48a81d34d898912aee6d6871cea88229a95a8707b8b57`  
		Last Modified: Thu, 29 May 2025 21:20:57 GMT  
		Size: 19.5 MB (19469837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a1808c79bcef7097281a639fc908523f3e2d89a1eed57fdd0a12ed08a3ec`  
		Last Modified: Thu, 29 May 2025 21:20:58 GMT  
		Size: 19.3 MB (19324587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca28ac16bb86e2f8eb95104f1683b2a0bd838e8dc7a20287a86909a84132cf72`  
		Last Modified: Thu, 29 May 2025 21:20:58 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4b6202c569c11174ecb9ae118d5e5fee60e0175b4c0e84757d68463a6ff719`  
		Last Modified: Thu, 29 May 2025 21:20:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be2ed86967b0fbde9f42a0846c21f323eb351896e0b26f137a12fddf4cee730`  
		Last Modified: Thu, 29 May 2025 21:20:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf8f6fc732cea121ee4629bfb674ca63158da7fdee6280680e87397e0a6a69`  
		Last Modified: Thu, 29 May 2025 22:07:27 GMT  
		Size: 7.0 MB (6978991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d736147cf5663e0edc1bdca7e92f9d49c5a32e401c740f19678b3bee49cd2e6`  
		Last Modified: Thu, 29 May 2025 22:07:27 GMT  
		Size: 99.4 KB (99399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c0076d70748e590a596a59d81ca92276d3962fa8630d51f5eeb6a8f7657352`  
		Last Modified: Thu, 29 May 2025 22:07:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0803cbf6896fa511fb04a35cfc0322f985dd33691cb462d97f83cd98cf716f`  
		Last Modified: Thu, 29 May 2025 22:07:29 GMT  
		Size: 57.2 MB (57152116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f76b3543e0e7dd8a5b0a5db6ae5faa55891f1d410f40f3e262577118a465c9`  
		Last Modified: Thu, 29 May 2025 22:07:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80961d6608cea20a13854996e91a7100a7b0952f7853652fa04cf9266ba0be53`  
		Last Modified: Thu, 29 May 2025 22:07:28 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9784576ab91c849043d55eb68529b29c2993d834d3018c97628f665ab64348`  
		Last Modified: Thu, 29 May 2025 22:27:52 GMT  
		Size: 1.0 MB (1014221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774e8e4aed242a170a1d03b742c177bd0b523062b9ce0748af4858e71126eb4f`  
		Last Modified: Thu, 29 May 2025 22:27:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e970bbd34adf6f44b06580c1617ada86665d05c64de31b966e5b9586978fd6`  
		Last Modified: Thu, 29 May 2025 22:27:51 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4512d97d8c84acc8522d89c773ddfc678915d4b78c8a846f0934df58b6a4ee2`  
		Last Modified: Thu, 29 May 2025 22:27:53 GMT  
		Size: 18.0 MB (18016124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f63e8fb274faddf751067fca0f80bb48fc8b6e6d65807463b18e01f6d4483`  
		Last Modified: Thu, 29 May 2025 22:27:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:17df46e9ff63d4d8e2b1aaafd811d8bd6b2f6346fbb951c29b00547150d2cec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3a187cc06b45e5844f01533a1e7706fc072c171981ba05716062b24dd1a11`

```dockerfile
```

-	Layers:
	-	`sha256:878b9843ebbdbba256239a28bad82a26fd0fc0d716954f65ae916f1f90cd41b0`  
		Last Modified: Thu, 29 May 2025 22:27:51 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json
