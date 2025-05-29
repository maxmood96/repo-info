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
-	[`docker:28.2`](#docker282)
-	[`docker:28.2-cli`](#docker282-cli)
-	[`docker:28.2-dind`](#docker282-dind)
-	[`docker:28.2-dind-rootless`](#docker282-dind-rootless)
-	[`docker:28.2-windowsservercore`](#docker282-windowsservercore)
-	[`docker:28.2-windowsservercore-1809`](#docker282-windowsservercore-1809)
-	[`docker:28.2-windowsservercore-ltsc2022`](#docker282-windowsservercore-ltsc2022)
-	[`docker:28.2-windowsservercore-ltsc2025`](#docker282-windowsservercore-ltsc2025)
-	[`docker:28.2.1`](#docker2821)
-	[`docker:28.2.1-alpine3.21`](#docker2821-alpine321)
-	[`docker:28.2.1-cli`](#docker2821-cli)
-	[`docker:28.2.1-cli-alpine3.21`](#docker2821-cli-alpine321)
-	[`docker:28.2.1-dind`](#docker2821-dind)
-	[`docker:28.2.1-dind-alpine3.21`](#docker2821-dind-alpine321)
-	[`docker:28.2.1-dind-rootless`](#docker2821-dind-rootless)
-	[`docker:28.2.1-windowsservercore`](#docker2821-windowsservercore)
-	[`docker:28.2.1-windowsservercore-1809`](#docker2821-windowsservercore-1809)
-	[`docker:28.2.1-windowsservercore-ltsc2022`](#docker2821-windowsservercore-ltsc2022)
-	[`docker:28.2.1-windowsservercore-ltsc2025`](#docker2821-windowsservercore-ltsc2025)
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
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:7ca534feede35eac86c4c3dac730f01a964b8d89459c14e87b76a428e188a7d5
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
$ docker pull docker@sha256:2c53ac6c5b8a191c626e34ca7f5ba51b5640702e8fb02053e4943a4b1e03db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1825d41f5972fd042124ed639974e3681b2d670343fc5d389df0b1b31fb68900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d742d2bd79f3cb86e2a70bfc95ff3df3c091a9eb06fa912ee4599513e5659f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17edaa4e07a03d6318d049c1312ddd6e08743bc8663ffa03f79bdcf30b19f6f1`

```dockerfile
```

-	Layers:
	-	`sha256:5bb285631254f0b58ac90d0f1ea9d2416b17451f51e8a06cda36ee7ab3d04d91`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4de2b813d19c2fc11c79969585be1237f0715bc522eef293f32b99756cbd3140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69211252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0d31b57db302a29e34c885b638aebf085e1e12b0843d96de74d3961c1cbcde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e51aee3758fe169aa7c7ed1bec3f7cba2912dd402bb2135b20151a76cc3d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4c1c81670072704c99e1d0793759c6e7fabb9903fa2596bdf192787e808400`

```dockerfile
```

-	Layers:
	-	`sha256:efc0982580efac57498955e4dab865d54485111344c12681801bc0df7cdbdae9`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:06d430157e2aa07b8352d9f854d2bc2f4062cca2e6d34f62f64b35487620bfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68220320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63624c9b1f9f2fb1bda80e1b523900f0fd459005a757ba686d789c56c2da174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4e63c852945c2e3237ba3ea0e12576f01296f49382c612adc2cfb21b9e0fe81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ad473a7702ad73a7eb68dd34071ec89afd5ea2fe9ee4bbc193ed23e5df75f`

```dockerfile
```

-	Layers:
	-	`sha256:ccc631a3495024199e0e49ae28c2b162ce0388b34eec5e325077e54703672861`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f0b8740eb162a8e44d25cb0a3b1538dc1ea342085aaefe07386af96e1b59bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69769433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7581f396878ba91b5ca7ab4915faa8fffc68e31e47adad23e8074502fa75c574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4dea99927f114f51ae34f8dd52e0805709a2a7e8ca360bb380c8c4d54db7eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc79369d1f8e33803276f77a6ce8f22f3b8fc092eb568beedd6b5484fd8054b8`

```dockerfile
```

-	Layers:
	-	`sha256:f94e0a32a4d561886c19f692cee849a546400d05b2f27169b185ea7f5accfb22`  
		Last Modified: Thu, 29 May 2025 21:20:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

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

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:e57684fc3b2f74bdd22440b46eb133fb888a6267a84f88e5e52d7ea5669ffc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:50b89b57d7960d9bd78fe1966dadaf99f605a783596b81d01e932f0667d4c81e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495966545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf0b8cc01679b55a8be2ae97414245f6c7d05f76345fb166d97f563ee8fed2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 29 May 2025 21:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:18:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:18:43 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:18:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:19:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:01 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:19:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:19:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:19:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:19:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:19:19 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b425300d422bcedb17fdac081e56acba744aaa3179f9da1d8d7b8fddb10a46b`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36bca8ee9252f9da40745bfce861c4cc10e65bda3728c6d0c8019e59517bcd`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 387.5 KB (387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221f32344eee0a8e7f8aa5517325387b1d2846e8383dc87d259f69d9d55f38b`  
		Last Modified: Thu, 29 May 2025 21:19:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f73ae5fbe5108eb9703e4f6f70385403b5aba7ea9d946d1f48cdbebfe5a99d6`  
		Last Modified: Thu, 29 May 2025 21:19:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50132a9a69dc44b9dd8b86cdb42d536a9bb08aa53f6525ea6abf5e7f706a58af`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 20.5 MB (20477283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4faa1e81dd6d1ddb45bd59df5b392afb9557f52975fd13adb299f126f1b8`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10e43b67386e4be1373fd0ec506f8ba502a359ef7a6002992258aea985f347`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42a09d52b077331ccf6d432bd3aa365e96f9809d39583afa99ecbf3b0db6b`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58593e0b25aa3f09a0a261473020d716203cac56eb0bead8ceda07c063f722`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.3 MB (22285611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8bde6d50e68a1120dea9bfecda7bbbb6482506da941f8a3bf0c43257670ce`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c467b6e16e4bbfa04c1917cf9dc320e009923a8de47f6bf801c9a0ccb3d42397`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568aa832f558e727179a9b7839fc88bfc1aea4ba4003da6369ca074999738f4`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df6139cc0973c8b6957a36a720f17dd3cf81c699926ecb2950b5a5b37fc499`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.0 MB (22038701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:e44dacda967bcfb8e86873b35a93069bd77ee0a23631222ba53cc2db46c843d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0bf48d9a532ee99590404446aa118456133cd1d185d833adbdc1651fc9775a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a880fab4ce0400e57a944477366f0290b8c2492f272af92cc91339d530ee3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:50b89b57d7960d9bd78fe1966dadaf99f605a783596b81d01e932f0667d4c81e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495966545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf0b8cc01679b55a8be2ae97414245f6c7d05f76345fb166d97f563ee8fed2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 29 May 2025 21:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:18:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:18:43 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:18:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:19:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:01 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:19:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:19:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:19:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:19:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:19:19 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b425300d422bcedb17fdac081e56acba744aaa3179f9da1d8d7b8fddb10a46b`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36bca8ee9252f9da40745bfce861c4cc10e65bda3728c6d0c8019e59517bcd`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 387.5 KB (387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221f32344eee0a8e7f8aa5517325387b1d2846e8383dc87d259f69d9d55f38b`  
		Last Modified: Thu, 29 May 2025 21:19:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f73ae5fbe5108eb9703e4f6f70385403b5aba7ea9d946d1f48cdbebfe5a99d6`  
		Last Modified: Thu, 29 May 2025 21:19:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50132a9a69dc44b9dd8b86cdb42d536a9bb08aa53f6525ea6abf5e7f706a58af`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 20.5 MB (20477283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4faa1e81dd6d1ddb45bd59df5b392afb9557f52975fd13adb299f126f1b8`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10e43b67386e4be1373fd0ec506f8ba502a359ef7a6002992258aea985f347`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42a09d52b077331ccf6d432bd3aa365e96f9809d39583afa99ecbf3b0db6b`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58593e0b25aa3f09a0a261473020d716203cac56eb0bead8ceda07c063f722`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.3 MB (22285611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8bde6d50e68a1120dea9bfecda7bbbb6482506da941f8a3bf0c43257670ce`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c467b6e16e4bbfa04c1917cf9dc320e009923a8de47f6bf801c9a0ccb3d42397`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568aa832f558e727179a9b7839fc88bfc1aea4ba4003da6369ca074999738f4`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df6139cc0973c8b6957a36a720f17dd3cf81c699926ecb2950b5a5b37fc499`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.0 MB (22038701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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

### `docker:28.2` - linux; amd64

```console
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-cli`

```console
$ docker pull docker@sha256:7ca534feede35eac86c4c3dac730f01a964b8d89459c14e87b76a428e188a7d5
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

### `docker:28.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:2c53ac6c5b8a191c626e34ca7f5ba51b5640702e8fb02053e4943a4b1e03db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1825d41f5972fd042124ed639974e3681b2d670343fc5d389df0b1b31fb68900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d742d2bd79f3cb86e2a70bfc95ff3df3c091a9eb06fa912ee4599513e5659f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17edaa4e07a03d6318d049c1312ddd6e08743bc8663ffa03f79bdcf30b19f6f1`

```dockerfile
```

-	Layers:
	-	`sha256:5bb285631254f0b58ac90d0f1ea9d2416b17451f51e8a06cda36ee7ab3d04d91`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4de2b813d19c2fc11c79969585be1237f0715bc522eef293f32b99756cbd3140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69211252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0d31b57db302a29e34c885b638aebf085e1e12b0843d96de74d3961c1cbcde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e51aee3758fe169aa7c7ed1bec3f7cba2912dd402bb2135b20151a76cc3d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4c1c81670072704c99e1d0793759c6e7fabb9903fa2596bdf192787e808400`

```dockerfile
```

-	Layers:
	-	`sha256:efc0982580efac57498955e4dab865d54485111344c12681801bc0df7cdbdae9`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:06d430157e2aa07b8352d9f854d2bc2f4062cca2e6d34f62f64b35487620bfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68220320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63624c9b1f9f2fb1bda80e1b523900f0fd459005a757ba686d789c56c2da174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4e63c852945c2e3237ba3ea0e12576f01296f49382c612adc2cfb21b9e0fe81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ad473a7702ad73a7eb68dd34071ec89afd5ea2fe9ee4bbc193ed23e5df75f`

```dockerfile
```

-	Layers:
	-	`sha256:ccc631a3495024199e0e49ae28c2b162ce0388b34eec5e325077e54703672861`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f0b8740eb162a8e44d25cb0a3b1538dc1ea342085aaefe07386af96e1b59bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69769433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7581f396878ba91b5ca7ab4915faa8fffc68e31e47adad23e8074502fa75c574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4dea99927f114f51ae34f8dd52e0805709a2a7e8ca360bb380c8c4d54db7eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc79369d1f8e33803276f77a6ce8f22f3b8fc092eb568beedd6b5484fd8054b8`

```dockerfile
```

-	Layers:
	-	`sha256:f94e0a32a4d561886c19f692cee849a546400d05b2f27169b185ea7f5accfb22`  
		Last Modified: Thu, 29 May 2025 21:20:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-dind`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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

### `docker:28.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-dind-rootless`

```console
$ docker pull docker@sha256:69d0d22b76699f0e1a25b983290b176121550f6563adcff0fa86b9ea2ffacae1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.2-dind-rootless` - linux; amd64

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

### `docker:28.2-dind-rootless` - unknown; unknown

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

### `docker:28.2-dind-rootless` - linux; arm64 variant v8

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

### `docker:28.2-dind-rootless` - unknown; unknown

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

## `docker:28.2-windowsservercore`

```console
$ docker pull docker@sha256:e57684fc3b2f74bdd22440b46eb133fb888a6267a84f88e5e52d7ea5669ffc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:28.2-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:50b89b57d7960d9bd78fe1966dadaf99f605a783596b81d01e932f0667d4c81e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495966545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf0b8cc01679b55a8be2ae97414245f6c7d05f76345fb166d97f563ee8fed2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 29 May 2025 21:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:18:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:18:43 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:18:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:19:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:01 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:19:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:19:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:19:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:19:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:19:19 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b425300d422bcedb17fdac081e56acba744aaa3179f9da1d8d7b8fddb10a46b`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36bca8ee9252f9da40745bfce861c4cc10e65bda3728c6d0c8019e59517bcd`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 387.5 KB (387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221f32344eee0a8e7f8aa5517325387b1d2846e8383dc87d259f69d9d55f38b`  
		Last Modified: Thu, 29 May 2025 21:19:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f73ae5fbe5108eb9703e4f6f70385403b5aba7ea9d946d1f48cdbebfe5a99d6`  
		Last Modified: Thu, 29 May 2025 21:19:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50132a9a69dc44b9dd8b86cdb42d536a9bb08aa53f6525ea6abf5e7f706a58af`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 20.5 MB (20477283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4faa1e81dd6d1ddb45bd59df5b392afb9557f52975fd13adb299f126f1b8`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10e43b67386e4be1373fd0ec506f8ba502a359ef7a6002992258aea985f347`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42a09d52b077331ccf6d432bd3aa365e96f9809d39583afa99ecbf3b0db6b`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58593e0b25aa3f09a0a261473020d716203cac56eb0bead8ceda07c063f722`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.3 MB (22285611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8bde6d50e68a1120dea9bfecda7bbbb6482506da941f8a3bf0c43257670ce`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c467b6e16e4bbfa04c1917cf9dc320e009923a8de47f6bf801c9a0ccb3d42397`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568aa832f558e727179a9b7839fc88bfc1aea4ba4003da6369ca074999738f4`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df6139cc0973c8b6957a36a720f17dd3cf81c699926ecb2950b5a5b37fc499`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.0 MB (22038701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.2-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.2-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2-windowsservercore-1809`

```console
$ docker pull docker@sha256:e44dacda967bcfb8e86873b35a93069bd77ee0a23631222ba53cc2db46c843d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:28.2-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0bf48d9a532ee99590404446aa118456133cd1d185d833adbdc1651fc9775a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28.2-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a880fab4ce0400e57a944477366f0290b8c2492f272af92cc91339d530ee3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:28.2-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:50b89b57d7960d9bd78fe1966dadaf99f605a783596b81d01e932f0667d4c81e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495966545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf0b8cc01679b55a8be2ae97414245f6c7d05f76345fb166d97f563ee8fed2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 29 May 2025 21:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:18:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:18:43 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:18:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:19:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:01 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:19:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:19:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:19:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:19:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:19:19 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b425300d422bcedb17fdac081e56acba744aaa3179f9da1d8d7b8fddb10a46b`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36bca8ee9252f9da40745bfce861c4cc10e65bda3728c6d0c8019e59517bcd`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 387.5 KB (387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221f32344eee0a8e7f8aa5517325387b1d2846e8383dc87d259f69d9d55f38b`  
		Last Modified: Thu, 29 May 2025 21:19:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f73ae5fbe5108eb9703e4f6f70385403b5aba7ea9d946d1f48cdbebfe5a99d6`  
		Last Modified: Thu, 29 May 2025 21:19:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50132a9a69dc44b9dd8b86cdb42d536a9bb08aa53f6525ea6abf5e7f706a58af`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 20.5 MB (20477283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4faa1e81dd6d1ddb45bd59df5b392afb9557f52975fd13adb299f126f1b8`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10e43b67386e4be1373fd0ec506f8ba502a359ef7a6002992258aea985f347`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42a09d52b077331ccf6d432bd3aa365e96f9809d39583afa99ecbf3b0db6b`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58593e0b25aa3f09a0a261473020d716203cac56eb0bead8ceda07c063f722`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.3 MB (22285611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8bde6d50e68a1120dea9bfecda7bbbb6482506da941f8a3bf0c43257670ce`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c467b6e16e4bbfa04c1917cf9dc320e009923a8de47f6bf801c9a0ccb3d42397`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568aa832f558e727179a9b7839fc88bfc1aea4ba4003da6369ca074999738f4`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df6139cc0973c8b6957a36a720f17dd3cf81c699926ecb2950b5a5b37fc499`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.0 MB (22038701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.1`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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

### `docker:28.2.1` - linux; amd64

```console
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:28.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:28.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.1-alpine3.21`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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

### `docker:28.2.1-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:28.2.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:28.2.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.1-cli`

```console
$ docker pull docker@sha256:7ca534feede35eac86c4c3dac730f01a964b8d89459c14e87b76a428e188a7d5
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

### `docker:28.2.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:2c53ac6c5b8a191c626e34ca7f5ba51b5640702e8fb02053e4943a4b1e03db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1825d41f5972fd042124ed639974e3681b2d670343fc5d389df0b1b31fb68900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d742d2bd79f3cb86e2a70bfc95ff3df3c091a9eb06fa912ee4599513e5659f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17edaa4e07a03d6318d049c1312ddd6e08743bc8663ffa03f79bdcf30b19f6f1`

```dockerfile
```

-	Layers:
	-	`sha256:5bb285631254f0b58ac90d0f1ea9d2416b17451f51e8a06cda36ee7ab3d04d91`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4de2b813d19c2fc11c79969585be1237f0715bc522eef293f32b99756cbd3140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69211252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0d31b57db302a29e34c885b638aebf085e1e12b0843d96de74d3961c1cbcde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e51aee3758fe169aa7c7ed1bec3f7cba2912dd402bb2135b20151a76cc3d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4c1c81670072704c99e1d0793759c6e7fabb9903fa2596bdf192787e808400`

```dockerfile
```

-	Layers:
	-	`sha256:efc0982580efac57498955e4dab865d54485111344c12681801bc0df7cdbdae9`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:06d430157e2aa07b8352d9f854d2bc2f4062cca2e6d34f62f64b35487620bfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68220320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63624c9b1f9f2fb1bda80e1b523900f0fd459005a757ba686d789c56c2da174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4e63c852945c2e3237ba3ea0e12576f01296f49382c612adc2cfb21b9e0fe81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ad473a7702ad73a7eb68dd34071ec89afd5ea2fe9ee4bbc193ed23e5df75f`

```dockerfile
```

-	Layers:
	-	`sha256:ccc631a3495024199e0e49ae28c2b162ce0388b34eec5e325077e54703672861`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f0b8740eb162a8e44d25cb0a3b1538dc1ea342085aaefe07386af96e1b59bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69769433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7581f396878ba91b5ca7ab4915faa8fffc68e31e47adad23e8074502fa75c574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4dea99927f114f51ae34f8dd52e0805709a2a7e8ca360bb380c8c4d54db7eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc79369d1f8e33803276f77a6ce8f22f3b8fc092eb568beedd6b5484fd8054b8`

```dockerfile
```

-	Layers:
	-	`sha256:f94e0a32a4d561886c19f692cee849a546400d05b2f27169b185ea7f5accfb22`  
		Last Modified: Thu, 29 May 2025 21:20:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.1-cli-alpine3.21`

```console
$ docker pull docker@sha256:7ca534feede35eac86c4c3dac730f01a964b8d89459c14e87b76a428e188a7d5
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

### `docker:28.2.1-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:2c53ac6c5b8a191c626e34ca7f5ba51b5640702e8fb02053e4943a4b1e03db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1825d41f5972fd042124ed639974e3681b2d670343fc5d389df0b1b31fb68900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:3d742d2bd79f3cb86e2a70bfc95ff3df3c091a9eb06fa912ee4599513e5659f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17edaa4e07a03d6318d049c1312ddd6e08743bc8663ffa03f79bdcf30b19f6f1`

```dockerfile
```

-	Layers:
	-	`sha256:5bb285631254f0b58ac90d0f1ea9d2416b17451f51e8a06cda36ee7ab3d04d91`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:4de2b813d19c2fc11c79969585be1237f0715bc522eef293f32b99756cbd3140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69211252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0d31b57db302a29e34c885b638aebf085e1e12b0843d96de74d3961c1cbcde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:e51aee3758fe169aa7c7ed1bec3f7cba2912dd402bb2135b20151a76cc3d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4c1c81670072704c99e1d0793759c6e7fabb9903fa2596bdf192787e808400`

```dockerfile
```

-	Layers:
	-	`sha256:efc0982580efac57498955e4dab865d54485111344c12681801bc0df7cdbdae9`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:06d430157e2aa07b8352d9f854d2bc2f4062cca2e6d34f62f64b35487620bfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68220320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63624c9b1f9f2fb1bda80e1b523900f0fd459005a757ba686d789c56c2da174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4e63c852945c2e3237ba3ea0e12576f01296f49382c612adc2cfb21b9e0fe81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ad473a7702ad73a7eb68dd34071ec89afd5ea2fe9ee4bbc193ed23e5df75f`

```dockerfile
```

-	Layers:
	-	`sha256:ccc631a3495024199e0e49ae28c2b162ce0388b34eec5e325077e54703672861`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f0b8740eb162a8e44d25cb0a3b1538dc1ea342085aaefe07386af96e1b59bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69769433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7581f396878ba91b5ca7ab4915faa8fffc68e31e47adad23e8074502fa75c574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:f4dea99927f114f51ae34f8dd52e0805709a2a7e8ca360bb380c8c4d54db7eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc79369d1f8e33803276f77a6ce8f22f3b8fc092eb568beedd6b5484fd8054b8`

```dockerfile
```

-	Layers:
	-	`sha256:f94e0a32a4d561886c19f692cee849a546400d05b2f27169b185ea7f5accfb22`  
		Last Modified: Thu, 29 May 2025 21:20:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.1-dind`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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

### `docker:28.2.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:28.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:28.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.1-dind-alpine3.21`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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

### `docker:28.2.1-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:28.2.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.1-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:28.2.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.1-dind-rootless`

```console
$ docker pull docker@sha256:69d0d22b76699f0e1a25b983290b176121550f6563adcff0fa86b9ea2ffacae1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.2.1-dind-rootless` - linux; amd64

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

### `docker:28.2.1-dind-rootless` - unknown; unknown

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

### `docker:28.2.1-dind-rootless` - linux; arm64 variant v8

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

### `docker:28.2.1-dind-rootless` - unknown; unknown

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

## `docker:28.2.1-windowsservercore`

```console
$ docker pull docker@sha256:e57684fc3b2f74bdd22440b46eb133fb888a6267a84f88e5e52d7ea5669ffc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:28.2.1-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:50b89b57d7960d9bd78fe1966dadaf99f605a783596b81d01e932f0667d4c81e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495966545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf0b8cc01679b55a8be2ae97414245f6c7d05f76345fb166d97f563ee8fed2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 29 May 2025 21:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:18:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:18:43 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:18:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:19:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:01 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:19:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:19:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:19:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:19:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:19:19 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b425300d422bcedb17fdac081e56acba744aaa3179f9da1d8d7b8fddb10a46b`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36bca8ee9252f9da40745bfce861c4cc10e65bda3728c6d0c8019e59517bcd`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 387.5 KB (387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221f32344eee0a8e7f8aa5517325387b1d2846e8383dc87d259f69d9d55f38b`  
		Last Modified: Thu, 29 May 2025 21:19:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f73ae5fbe5108eb9703e4f6f70385403b5aba7ea9d946d1f48cdbebfe5a99d6`  
		Last Modified: Thu, 29 May 2025 21:19:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50132a9a69dc44b9dd8b86cdb42d536a9bb08aa53f6525ea6abf5e7f706a58af`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 20.5 MB (20477283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4faa1e81dd6d1ddb45bd59df5b392afb9557f52975fd13adb299f126f1b8`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10e43b67386e4be1373fd0ec506f8ba502a359ef7a6002992258aea985f347`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42a09d52b077331ccf6d432bd3aa365e96f9809d39583afa99ecbf3b0db6b`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58593e0b25aa3f09a0a261473020d716203cac56eb0bead8ceda07c063f722`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.3 MB (22285611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8bde6d50e68a1120dea9bfecda7bbbb6482506da941f8a3bf0c43257670ce`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c467b6e16e4bbfa04c1917cf9dc320e009923a8de47f6bf801c9a0ccb3d42397`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568aa832f558e727179a9b7839fc88bfc1aea4ba4003da6369ca074999738f4`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df6139cc0973c8b6957a36a720f17dd3cf81c699926ecb2950b5a5b37fc499`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.0 MB (22038701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.2.1-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.2.1-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:e44dacda967bcfb8e86873b35a93069bd77ee0a23631222ba53cc2db46c843d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:28.2.1-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0bf48d9a532ee99590404446aa118456133cd1d185d833adbdc1651fc9775a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28.2.1-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a880fab4ce0400e57a944477366f0290b8c2492f272af92cc91339d530ee3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:28.2.1-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:50b89b57d7960d9bd78fe1966dadaf99f605a783596b81d01e932f0667d4c81e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495966545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf0b8cc01679b55a8be2ae97414245f6c7d05f76345fb166d97f563ee8fed2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 29 May 2025 21:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:18:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:18:43 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:18:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:19:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:01 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:19:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:19:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:19:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:19:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:19:19 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b425300d422bcedb17fdac081e56acba744aaa3179f9da1d8d7b8fddb10a46b`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36bca8ee9252f9da40745bfce861c4cc10e65bda3728c6d0c8019e59517bcd`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 387.5 KB (387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221f32344eee0a8e7f8aa5517325387b1d2846e8383dc87d259f69d9d55f38b`  
		Last Modified: Thu, 29 May 2025 21:19:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f73ae5fbe5108eb9703e4f6f70385403b5aba7ea9d946d1f48cdbebfe5a99d6`  
		Last Modified: Thu, 29 May 2025 21:19:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50132a9a69dc44b9dd8b86cdb42d536a9bb08aa53f6525ea6abf5e7f706a58af`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 20.5 MB (20477283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4faa1e81dd6d1ddb45bd59df5b392afb9557f52975fd13adb299f126f1b8`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10e43b67386e4be1373fd0ec506f8ba502a359ef7a6002992258aea985f347`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42a09d52b077331ccf6d432bd3aa365e96f9809d39583afa99ecbf3b0db6b`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58593e0b25aa3f09a0a261473020d716203cac56eb0bead8ceda07c063f722`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.3 MB (22285611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8bde6d50e68a1120dea9bfecda7bbbb6482506da941f8a3bf0c43257670ce`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c467b6e16e4bbfa04c1917cf9dc320e009923a8de47f6bf801c9a0ccb3d42397`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568aa832f558e727179a9b7839fc88bfc1aea4ba4003da6369ca074999738f4`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df6139cc0973c8b6957a36a720f17dd3cf81c699926ecb2950b5a5b37fc499`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.0 MB (22038701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:7ca534feede35eac86c4c3dac730f01a964b8d89459c14e87b76a428e188a7d5
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
$ docker pull docker@sha256:2c53ac6c5b8a191c626e34ca7f5ba51b5640702e8fb02053e4943a4b1e03db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1825d41f5972fd042124ed639974e3681b2d670343fc5d389df0b1b31fb68900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d742d2bd79f3cb86e2a70bfc95ff3df3c091a9eb06fa912ee4599513e5659f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17edaa4e07a03d6318d049c1312ddd6e08743bc8663ffa03f79bdcf30b19f6f1`

```dockerfile
```

-	Layers:
	-	`sha256:5bb285631254f0b58ac90d0f1ea9d2416b17451f51e8a06cda36ee7ab3d04d91`  
		Last Modified: Thu, 29 May 2025 21:13:27 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4de2b813d19c2fc11c79969585be1237f0715bc522eef293f32b99756cbd3140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69211252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0d31b57db302a29e34c885b638aebf085e1e12b0843d96de74d3961c1cbcde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e51aee3758fe169aa7c7ed1bec3f7cba2912dd402bb2135b20151a76cc3d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4c1c81670072704c99e1d0793759c6e7fabb9903fa2596bdf192787e808400`

```dockerfile
```

-	Layers:
	-	`sha256:efc0982580efac57498955e4dab865d54485111344c12681801bc0df7cdbdae9`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:06d430157e2aa07b8352d9f854d2bc2f4062cca2e6d34f62f64b35487620bfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68220320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63624c9b1f9f2fb1bda80e1b523900f0fd459005a757ba686d789c56c2da174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4e63c852945c2e3237ba3ea0e12576f01296f49382c612adc2cfb21b9e0fe81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ad473a7702ad73a7eb68dd34071ec89afd5ea2fe9ee4bbc193ed23e5df75f`

```dockerfile
```

-	Layers:
	-	`sha256:ccc631a3495024199e0e49ae28c2b162ce0388b34eec5e325077e54703672861`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f0b8740eb162a8e44d25cb0a3b1538dc1ea342085aaefe07386af96e1b59bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69769433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7581f396878ba91b5ca7ab4915faa8fffc68e31e47adad23e8074502fa75c574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4dea99927f114f51ae34f8dd52e0805709a2a7e8ca360bb380c8c4d54db7eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc79369d1f8e33803276f77a6ce8f22f3b8fc092eb568beedd6b5484fd8054b8`

```dockerfile
```

-	Layers:
	-	`sha256:f94e0a32a4d561886c19f692cee849a546400d05b2f27169b185ea7f5accfb22`  
		Last Modified: Thu, 29 May 2025 21:20:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:69d0d22b76699f0e1a25b983290b176121550f6563adcff0fa86b9ea2ffacae1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

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

### `docker:dind-rootless` - unknown; unknown

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

### `docker:dind-rootless` - linux; arm64 variant v8

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

### `docker:dind-rootless` - unknown; unknown

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

## `docker:latest`

```console
$ docker pull docker@sha256:4610d33c9a2b9c2bce10ce76c693ee7564506845dd190deb80c3c3afbb62296d
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
$ docker pull docker@sha256:f08155995ca66d82df7d2436492f50dfe6046a900cfc6dbcbf487ce9ee5d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143180242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522e6c6e175d8135e350f8c481e9ae4de71904bfb525b7049e54033b5ad7ba1`
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:18152deb2a1f6e6698a03bd02b4b647e07051f0610b28354f87dbee0eea5704d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98eab3f86686bbb5abaad258928ae016e6596d02aaebbc1d1107660fc2296e`

```dockerfile
```

-	Layers:
	-	`sha256:f24cb1fc9bdde9df106203df20a75eebc272a434c0a4c46d6fb1b83fcd0ed04e`  
		Last Modified: Thu, 29 May 2025 22:07:46 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:7ddabcdb433ddb8b2cb87f355623edb0b38cb2f2df20d86b9fd78f6958ae6a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134225393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aabd8ce66d4702e8f4ff25c6d9b6048917b4a03d7464d8f949773ff7a7c14e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd839f64baff9927abbc58f21e00a26012fed513677d0a9c52ef3af98f6a497`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18101933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19095d8616290327c3d0e9c79646a6e8a73d254ce5f66c8d76450d3868c4981c`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19943306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b923bf21b53e62fe10fc61ca9c9e6ce1c24f9a4305830422a3d30f53fb161a7`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19820981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0babba5b7d35ed22ff8850f5f29ab08b93d6a7e6d4936dea2fa826b4a5b9839e`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d3bf27d088cef0c4e93b28e4b13617c22f455d68e7511558ea41c3a2ba39`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef57afdbdb11b91e067d39cf160efbdc0e03db35670334890cc84a95f5e5e2d`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 7.0 MB (7036896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b0d78c48d140b5d27338d4b03d1d9dba60233f604e9483e00136153441a1c`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012586c49bd2ac5492dde17f22e8ba7a41372e23daee816456e42f6e40c31bf`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f5c1dd681750c457ebb455e1b0b695c61991f652a3c669b820d49f88c830c`  
		Last Modified: Thu, 29 May 2025 21:14:24 GMT  
		Size: 57.9 MB (57881360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2860150b54b77c2f659c8e9700f9aa285936665b2ec511516421704b8fcebd5`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbcd1cac502c9c054cee68dd0374ed55722c1da2fd05ca771054620eb3f80e`  
		Last Modified: Thu, 29 May 2025 21:14:23 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:7dd366a721c2c54845e13fa3016d50951544c8a246baa24e92cecbd4acedc3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38329f8baf5eeacc7b50a42b04477ca2651b14d9d27457b875c745e3b8eef92`

```dockerfile
```

-	Layers:
	-	`sha256:6244fa1256704447c3442c083292cd924bbec9e09387226901d647631d3df077`  
		Last Modified: Thu, 29 May 2025 21:14:22 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:d1ccb1ab4211cf5275680c9fcf693b781de03487c4827cb9ea2a611a3dc33a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199a4cf96adf56687b3d4b9e32104dd29c604ae81fe34f52b79f2d058bb6e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f8628f199cc7b24253f03a0dc7ba737601df99c05082f973ca13d262aeebd`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00b233e1abe4ced27f55e69e0d38a450c6833cd9bdc7a076b2cc828926f462`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.9 MB (19927220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3ac28b4650ae86afeba82a0ac6308d45b24dc124cdc9ada817b3c9b932b14`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32e9ea370d4b617cb656ae022312af9d0255cb48602396e61415431756bf7e`  
		Last Modified: Thu, 29 May 2025 21:13:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c1fef0c14b4307ca6c06af2a079532c3d01a0e52ba1a1a4f2e73790947bbb`  
		Last Modified: Thu, 29 May 2025 21:13:10 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776369c351443b3d9bfd5a8893cb2ca72cc1057975589d33e40ad1a9aa24b63`  
		Last Modified: Thu, 29 May 2025 21:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad8093dea5eb8a6f72347f8f17dae954ac92f732368ab69b22cb698b68e58f`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 6.4 MB (6366162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3bbb0444d4cc4e718d8ececa6d4fbf4d4503f2a73d66071e5ece362a2b379`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b3aec16f4fc81f37643d73fc5e5c23aee885b6e26cacca2b9108e92f9e613`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b725948ba7fa339adb7e4b7632c68787e84d99a5fd21335411a3d846361e9c`  
		Last Modified: Thu, 29 May 2025 21:14:30 GMT  
		Size: 57.9 MB (57881383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd29f2e8843f0e31f6047dacd8f58b4bf7987b95ea57cab22010a16ca8ebed`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bccfa75343be0a95be94eed373abd8a28f0e82e90d3d67e5b72319c661f2`  
		Last Modified: Thu, 29 May 2025 21:14:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3ee792a426e41c07491f0aee2f0e369aee04c473a26d0956a838a25901c72786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739cd2314fbb002a311aec1fce112c3d6943edb67ad29bb2c834d9ab07ce32d4`

```dockerfile
```

-	Layers:
	-	`sha256:1ebadb0181a56346258a185ca775bfb90d2e4410702bf01584cedf367318e23d`  
		Last Modified: Thu, 29 May 2025 21:14:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c7afaa8a478ae2b724ae9a52941635a1e51cab0e1aeae15e5673cc2d9e742226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134005936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd95b007c0e2375664122dee2b6d83ae9cbdfc365e1ebdc9aaff4cb3a3d258`
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:4fe6280236984c09c499897c3df888ef5707437ed462387aff9450f88ec7f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2406cc1f83865c64eb21a4c9ab6ee428971c92b4f0fce1d0c89890b352a150f6`

```dockerfile
```

-	Layers:
	-	`sha256:6e0dba0304796697b97fa3218ac557a0b221415da49b3237056c6c290160e60e`  
		Last Modified: Thu, 29 May 2025 22:07:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e57684fc3b2f74bdd22440b46eb133fb888a6267a84f88e5e52d7ea5669ffc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:50b89b57d7960d9bd78fe1966dadaf99f605a783596b81d01e932f0667d4c81e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495966545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf0b8cc01679b55a8be2ae97414245f6c7d05f76345fb166d97f563ee8fed2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 29 May 2025 21:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:18:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:18:43 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:18:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:19:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:01 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:19:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:19:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:19:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:19:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:19:19 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b425300d422bcedb17fdac081e56acba744aaa3179f9da1d8d7b8fddb10a46b`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36bca8ee9252f9da40745bfce861c4cc10e65bda3728c6d0c8019e59517bcd`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 387.5 KB (387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221f32344eee0a8e7f8aa5517325387b1d2846e8383dc87d259f69d9d55f38b`  
		Last Modified: Thu, 29 May 2025 21:19:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f73ae5fbe5108eb9703e4f6f70385403b5aba7ea9d946d1f48cdbebfe5a99d6`  
		Last Modified: Thu, 29 May 2025 21:19:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50132a9a69dc44b9dd8b86cdb42d536a9bb08aa53f6525ea6abf5e7f706a58af`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 20.5 MB (20477283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4faa1e81dd6d1ddb45bd59df5b392afb9557f52975fd13adb299f126f1b8`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10e43b67386e4be1373fd0ec506f8ba502a359ef7a6002992258aea985f347`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42a09d52b077331ccf6d432bd3aa365e96f9809d39583afa99ecbf3b0db6b`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58593e0b25aa3f09a0a261473020d716203cac56eb0bead8ceda07c063f722`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.3 MB (22285611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8bde6d50e68a1120dea9bfecda7bbbb6482506da941f8a3bf0c43257670ce`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c467b6e16e4bbfa04c1917cf9dc320e009923a8de47f6bf801c9a0ccb3d42397`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568aa832f558e727179a9b7839fc88bfc1aea4ba4003da6369ca074999738f4`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df6139cc0973c8b6957a36a720f17dd3cf81c699926ecb2950b5a5b37fc499`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.0 MB (22038701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:e44dacda967bcfb8e86873b35a93069bd77ee0a23631222ba53cc2db46c843d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:b6f0521aec34684e7b422c0a914fd815ced0128b7f13f4bbe7763275624c7baf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248820442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e7f15905f4ed116fb5bcc897ca471e273def5529ec95a6838e5c13c16e8d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 29 May 2025 21:21:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:22:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:22:42 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:22:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:22:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:22:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:23:00 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:23:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:23:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:23:10 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:23:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6046c800b6f37acb68e3dc9bc5c8eabada7b62c03e33cac7e00290bf1175234`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fb86d7b162c7b698e841f55a018fe47aa94e7dda5ef3e2c58190d379b03bc0`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4885bee43d0bd1d0d67131ac9647e7279644b4412b8f423d7ac0d298571143a`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a22398b3434bc6d844b469d7f4bde820c4393b323f0296382a9e4fd03b0cb9`  
		Last Modified: Thu, 29 May 2025 21:23:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d056634bc80b18bc3d7621dfda6c196bfff55019ba243dfe84a85048d8a1a`  
		Last Modified: Thu, 29 May 2025 21:23:25 GMT  
		Size: 20.5 MB (20457730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a24afdb3b0a22bc65c986eccb734e0b8a8bf4765e707af468832fdb2efedef`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edfa0c0f3962af71f135add34ee59282d1046158dd3221c6e77c78d19e3ed`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e841a4b5fb0e3f52d9873cdf8ee88e61a2966db2a33e6a6d77f3de8ab1f61aba`  
		Last Modified: Thu, 29 May 2025 21:23:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effd6519b77fdbbbbdcd72e2804b94d1729cc4f3e5b49165d3c16280d2fe8420`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.3 MB (22264763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26520c3a4c34da2db545d670da3308405c909150da375e9b223a3ef0169879`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4ef84f583bb16523dda059aaa5dd12b3a112c231c3a8a4ba679c077ac3ec6e`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1735a07b3794b3a1f15df315efa629c685402b2f7f2e9292fd439fa08e9b0`  
		Last Modified: Thu, 29 May 2025 21:23:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce117d95e87c381e39efc10a6c53c09c1a62348ec02e30379885e7e65fd602a`  
		Last Modified: Thu, 29 May 2025 21:23:24 GMT  
		Size: 22.0 MB (22006700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0bf48d9a532ee99590404446aa118456133cd1d185d833adbdc1651fc9775a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a880fab4ce0400e57a944477366f0290b8c2492f272af92cc91339d530ee3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:50b89b57d7960d9bd78fe1966dadaf99f605a783596b81d01e932f0667d4c81e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495966545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bf0b8cc01679b55a8be2ae97414245f6c7d05f76345fb166d97f563ee8fed2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 29 May 2025 21:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:18:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:18:43 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:18:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:19:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:01 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:19:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:19:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:19:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:19:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:19:19 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b425300d422bcedb17fdac081e56acba744aaa3179f9da1d8d7b8fddb10a46b`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36bca8ee9252f9da40745bfce861c4cc10e65bda3728c6d0c8019e59517bcd`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 387.5 KB (387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221f32344eee0a8e7f8aa5517325387b1d2846e8383dc87d259f69d9d55f38b`  
		Last Modified: Thu, 29 May 2025 21:19:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f73ae5fbe5108eb9703e4f6f70385403b5aba7ea9d946d1f48cdbebfe5a99d6`  
		Last Modified: Thu, 29 May 2025 21:19:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50132a9a69dc44b9dd8b86cdb42d536a9bb08aa53f6525ea6abf5e7f706a58af`  
		Last Modified: Thu, 29 May 2025 21:19:38 GMT  
		Size: 20.5 MB (20477283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4faa1e81dd6d1ddb45bd59df5b392afb9557f52975fd13adb299f126f1b8`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10e43b67386e4be1373fd0ec506f8ba502a359ef7a6002992258aea985f347`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42a09d52b077331ccf6d432bd3aa365e96f9809d39583afa99ecbf3b0db6b`  
		Last Modified: Thu, 29 May 2025 21:19:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58593e0b25aa3f09a0a261473020d716203cac56eb0bead8ceda07c063f722`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.3 MB (22285611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8bde6d50e68a1120dea9bfecda7bbbb6482506da941f8a3bf0c43257670ce`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c467b6e16e4bbfa04c1917cf9dc320e009923a8de47f6bf801c9a0ccb3d42397`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5568aa832f558e727179a9b7839fc88bfc1aea4ba4003da6369ca074999738f4`  
		Last Modified: Thu, 29 May 2025 21:19:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df6139cc0973c8b6957a36a720f17dd3cf81c699926ecb2950b5a5b37fc499`  
		Last Modified: Thu, 29 May 2025 21:19:35 GMT  
		Size: 22.0 MB (22038701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
