## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:97812aadadc54becb802e1781455856ea3e722a42fb74dd0dfb03097bd954d2a
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
$ docker pull docker@sha256:0e7d9f4a6504a9186c8050383f64e6e54371898615d5a07fbf4fd41725144579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152469192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3935173f00b14d546f527d8d55b84adef198749b08f17652765681726f546d2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c10540f66ae08ba872ef0b8b2ac5b0d8e2f734d49953d9866543cfd19298f`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 7.0 MB (6978936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c23c50e160dba55151940d23aa190841f10bca12a34b34b1a3129ae4f57a89`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 99.4 KB (99398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c3b2576819b89a08031e832bba46a29d5dd1ff310dfbd2b5b94a2989bb3d7e`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103a2dd279a848eae5a76703c3da8acac2fbd215dcf30a0a85aa3d028c8b3a0`  
		Last Modified: Fri, 23 May 2025 19:07:43 GMT  
		Size: 55.7 MB (55740981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d126e1c1bb1a79f07755473da059e7462ddf04a567a1f23e35f00c3061c9bed`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371388cdf0d156bde8edbfdf54112cd6070593421a693de91426ab1d006f3ec3`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b167f53dbc3c10a0fee54cd2fbc21c63ef560ccfbaf70a5eb637eb6ee9232c`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 1.0 MB (1014221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28433ac331737f34dbbe50ca0d68fe786412a83cfae898842b93fee6f83c0629`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e732c11713043a1eb8eace9f1d8a37ae40d750048f70a7b2ffeda99d6f7f32`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b43a91dd2d769b9dafcdc38404aa1312f51239bf23b9d7d691cd5591ee3ba`  
		Last Modified: Fri, 23 May 2025 19:11:14 GMT  
		Size: 19.3 MB (19275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8897570bceeb3a64d126c34833b4fb058d296ba8fa13c7a8e253e9d9b83a40a`  
		Last Modified: Fri, 23 May 2025 19:11:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d1438b41e0f227d68b064f2965104ae8e831821e6ec2ec7a1023df4de92f31af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e127ef7c7db9e45d20ddf05ab157ed4d70b5d592716308ef635ec465915d1af`

```dockerfile
```

-	Layers:
	-	`sha256:a201eb3d474956b219bc5733079966db14d7278d36a20ee198b03780dd3fe45a`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json
