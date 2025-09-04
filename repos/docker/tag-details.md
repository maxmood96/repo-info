<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.4`](#docker284)
-	[`docker:28.4-cli`](#docker284-cli)
-	[`docker:28.4-dind`](#docker284-dind)
-	[`docker:28.4-dind-rootless`](#docker284-dind-rootless)
-	[`docker:28.4-windowsservercore`](#docker284-windowsservercore)
-	[`docker:28.4-windowsservercore-ltsc2022`](#docker284-windowsservercore-ltsc2022)
-	[`docker:28.4-windowsservercore-ltsc2025`](#docker284-windowsservercore-ltsc2025)
-	[`docker:28.4.0`](#docker2840)
-	[`docker:28.4.0-alpine3.22`](#docker2840-alpine322)
-	[`docker:28.4.0-cli`](#docker2840-cli)
-	[`docker:28.4.0-cli-alpine3.22`](#docker2840-cli-alpine322)
-	[`docker:28.4.0-dind`](#docker2840-dind)
-	[`docker:28.4.0-dind-alpine3.22`](#docker2840-dind-alpine322)
-	[`docker:28.4.0-dind-rootless`](#docker2840-dind-rootless)
-	[`docker:28.4.0-windowsservercore`](#docker2840-windowsservercore)
-	[`docker:28.4.0-windowsservercore-ltsc2022`](#docker2840-windowsservercore-ltsc2022)
-	[`docker:28.4.0-windowsservercore-ltsc2025`](#docker2840-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:0b928cff9f8f13b3475054da4af345db6b21007865f4fa3e0602b4422fea5f99
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
$ docker pull docker@sha256:73e41535043067691a7c87773c5185aa2d2bcf70da2770f878b1e31e13054980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76019659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056e2811a4634c5a0f25fe0954b56f24c25f926aeb1223b8952570b6c8713db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1bc58cae8b64023ff83a66e3e6c7a010244c2d0b37b31569b7410a3d0f160572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e4aa4c316414f5fda3df8b4df63fb46aa181d21ec0e7d5d2fd69b2b2a2deb9`

```dockerfile
```

-	Layers:
	-	`sha256:9949e013047bd65e547eba6bfd2cee9632caa48928b88b2cd515523f27aeb42b`  
		Last Modified: Thu, 04 Sep 2025 17:07:51 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad6e8b9bcb81416a9db3d34d65430e10e47acbcf37a4c9cf0db5c9a955a4e2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70947926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32618647e86987ce8f9b539cb4d3214f258794be577a61c143929f86609d52be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2421e5297d31e7232bf7c1ef83de638ab7a70e69240db127e82a42cc6255de18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1df48c0d35c4804846bf1c564dbdf23bbb014a90287637c98881ad47ad389c`

```dockerfile
```

-	Layers:
	-	`sha256:be8f9e60ee07824b3be12bd4898912592e94f0206efe05bbd40ca108856b2fc6`  
		Last Modified: Thu, 04 Sep 2025 17:07:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:36a89a541df1c76536798d2c70834c2a684fc40cd367da1991b38773b6687879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69940868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a8ff797b7c1f2e5c72cd2e8eb9736e52a036027dd8d9aac4ffb3a8fb99675b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6f52417beefc84301e134d1e6074194516b2daec77852e0c383b8c6cb8f3b6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcd14439dffea87510fd977e9a07dbfaf9bfcc03d46cb079c0459510051a3b`

```dockerfile
```

-	Layers:
	-	`sha256:442e4a644798d56efd70101e28ec5051f693ae9aa65ad0cb959bdac4c1ee77e7`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:124a8198af1cac6c30a13ea821f254b8699238d1c4d70212f689a2925b545233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71511020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb87a098f7d537ae39f72ab097a2a832e6ac09952042f6ee35eb0f760a16cc4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:90e3a9d1cb67f41875d2444f7b9cd67305425a82209e5debc8b0619d8b1c503b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386a491cf42f7a37851ceb04365b5fffec1b7efd6a6d0a3edb63fa41b885a63`

```dockerfile
```

-	Layers:
	-	`sha256:8ce75e56843ed96155ce89b112cae5e76e26f78cac99fea643694ce2aedc3459`  
		Last Modified: Thu, 04 Sep 2025 17:08:03 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:4862cd916195b0e7a7823515ca74affdcbd259918bb393cae4480c8bf211a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3f6dd9dda95b8304f0d036045003a1ac2625d92a6d53abf88ebad522cce9ed34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169388498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e46e4df60bfaa2236d3fcb2933590c4331b5f66aacb86dd1a97cfd46e1cf59`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a220c8ec60c5c78af9d030015dbffc31df5f98bcb7ac9ed549068111713bd486`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 3.4 MB (3398455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdd74c6da8fedbd70ae176c68e2d0d3bf14c0f0ecca6859bb922b058cab0922`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b268299b4c1e90c236d9c1877cc2a56354da68eb7a9e6a06279c3f4d4ff32`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ede92035dcbd5985ddf6cada9ed6941caf4f53d763c83ab9e57f0c1eb8ee9c`  
		Last Modified: Thu, 04 Sep 2025 16:47:56 GMT  
		Size: 17.6 MB (17592033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2ec14a93ab2f5b33b5f9018640084359cea86ce9e2cedb1aa87187032d75f9`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6de2e74c4d99f16e038921cee84a89f66812e2a39c258d4d7ceb1be228d93ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5931ec4a77c8b88fbba7ebd8174da2c66e2819353e92d90f2782fe61832e56`

```dockerfile
```

-	Layers:
	-	`sha256:b863adb3de5876cea71f942b3f7285aa107d60c284402c23953e77dd172a8791`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d5e35da919bf42c0995a57696f671d0295d480843e1b5c20fac8f180cc48c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160766167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e05fa41c1eda1bed27053bbef7d3330dfc7e9105c90eb3d1fd24b2509a388bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131fba448ae92cbd556ec5ae35286e170ca8d311754dee6af2dfc86d1f65653a`  
		Last Modified: Thu, 04 Sep 2025 16:47:16 GMT  
		Size: 3.4 MB (3390000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69c261a333123ee40938fa92f27b1d435e8ad7aad5212b89bebe490a613c636`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6bb051de3347c4d9049437be002ba818cd4f1d417ded7bd9faf3f2b6535baf`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13de9e382c27e5047737dfd2867d0d0cf0e8dd013f07c7be50b1e1a1dd800b37`  
		Last Modified: Thu, 04 Sep 2025 16:47:17 GMT  
		Size: 18.0 MB (18019443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721bf468705703556597d579c203b456cfe2722911b77c2d6b7903e4b8aae0a7`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:909cc8c4892e1607ffe7af2d231cb7e71effafc5a8752d267c0552e5f38bb0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07776a92b2e62dd43552588556afcba5e689d4f7e859ea02649abf7aa3d7845a`

```dockerfile
```

-	Layers:
	-	`sha256:2f02297fd46c6856422b935bcbcf389d235b7479989d9b858119d5a7f6275947`  
		Last Modified: Thu, 04 Sep 2025 17:08:01 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:d310dcc104666bdc130f204f4b9d1fb7341508a9710b53a056e440710d60c667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:875b4a57683b8cadc534c38b1a458b26f0ee03a02226ce29d1835369156f7bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:00efa870cb48d2587069580480eec0b1dbf1481faa14c899a74fc786b18562cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.4`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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

### `docker:28.4` - linux; amd64

```console
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4-cli`

```console
$ docker pull docker@sha256:0b928cff9f8f13b3475054da4af345db6b21007865f4fa3e0602b4422fea5f99
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

### `docker:28.4-cli` - linux; amd64

```console
$ docker pull docker@sha256:73e41535043067691a7c87773c5185aa2d2bcf70da2770f878b1e31e13054980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76019659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056e2811a4634c5a0f25fe0954b56f24c25f926aeb1223b8952570b6c8713db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1bc58cae8b64023ff83a66e3e6c7a010244c2d0b37b31569b7410a3d0f160572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e4aa4c316414f5fda3df8b4df63fb46aa181d21ec0e7d5d2fd69b2b2a2deb9`

```dockerfile
```

-	Layers:
	-	`sha256:9949e013047bd65e547eba6bfd2cee9632caa48928b88b2cd515523f27aeb42b`  
		Last Modified: Thu, 04 Sep 2025 17:07:51 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad6e8b9bcb81416a9db3d34d65430e10e47acbcf37a4c9cf0db5c9a955a4e2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70947926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32618647e86987ce8f9b539cb4d3214f258794be577a61c143929f86609d52be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2421e5297d31e7232bf7c1ef83de638ab7a70e69240db127e82a42cc6255de18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1df48c0d35c4804846bf1c564dbdf23bbb014a90287637c98881ad47ad389c`

```dockerfile
```

-	Layers:
	-	`sha256:be8f9e60ee07824b3be12bd4898912592e94f0206efe05bbd40ca108856b2fc6`  
		Last Modified: Thu, 04 Sep 2025 17:07:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:36a89a541df1c76536798d2c70834c2a684fc40cd367da1991b38773b6687879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69940868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a8ff797b7c1f2e5c72cd2e8eb9736e52a036027dd8d9aac4ffb3a8fb99675b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6f52417beefc84301e134d1e6074194516b2daec77852e0c383b8c6cb8f3b6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcd14439dffea87510fd977e9a07dbfaf9bfcc03d46cb079c0459510051a3b`

```dockerfile
```

-	Layers:
	-	`sha256:442e4a644798d56efd70101e28ec5051f693ae9aa65ad0cb959bdac4c1ee77e7`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:124a8198af1cac6c30a13ea821f254b8699238d1c4d70212f689a2925b545233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71511020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb87a098f7d537ae39f72ab097a2a832e6ac09952042f6ee35eb0f760a16cc4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:90e3a9d1cb67f41875d2444f7b9cd67305425a82209e5debc8b0619d8b1c503b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386a491cf42f7a37851ceb04365b5fffec1b7efd6a6d0a3edb63fa41b885a63`

```dockerfile
```

-	Layers:
	-	`sha256:8ce75e56843ed96155ce89b112cae5e76e26f78cac99fea643694ce2aedc3459`  
		Last Modified: Thu, 04 Sep 2025 17:08:03 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4-dind`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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

### `docker:28.4-dind` - linux; amd64

```console
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4-dind-rootless`

```console
$ docker pull docker@sha256:4862cd916195b0e7a7823515ca74affdcbd259918bb393cae4480c8bf211a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.4-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3f6dd9dda95b8304f0d036045003a1ac2625d92a6d53abf88ebad522cce9ed34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169388498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e46e4df60bfaa2236d3fcb2933590c4331b5f66aacb86dd1a97cfd46e1cf59`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a220c8ec60c5c78af9d030015dbffc31df5f98bcb7ac9ed549068111713bd486`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 3.4 MB (3398455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdd74c6da8fedbd70ae176c68e2d0d3bf14c0f0ecca6859bb922b058cab0922`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b268299b4c1e90c236d9c1877cc2a56354da68eb7a9e6a06279c3f4d4ff32`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ede92035dcbd5985ddf6cada9ed6941caf4f53d763c83ab9e57f0c1eb8ee9c`  
		Last Modified: Thu, 04 Sep 2025 16:47:56 GMT  
		Size: 17.6 MB (17592033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2ec14a93ab2f5b33b5f9018640084359cea86ce9e2cedb1aa87187032d75f9`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6de2e74c4d99f16e038921cee84a89f66812e2a39c258d4d7ceb1be228d93ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5931ec4a77c8b88fbba7ebd8174da2c66e2819353e92d90f2782fe61832e56`

```dockerfile
```

-	Layers:
	-	`sha256:b863adb3de5876cea71f942b3f7285aa107d60c284402c23953e77dd172a8791`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d5e35da919bf42c0995a57696f671d0295d480843e1b5c20fac8f180cc48c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160766167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e05fa41c1eda1bed27053bbef7d3330dfc7e9105c90eb3d1fd24b2509a388bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131fba448ae92cbd556ec5ae35286e170ca8d311754dee6af2dfc86d1f65653a`  
		Last Modified: Thu, 04 Sep 2025 16:47:16 GMT  
		Size: 3.4 MB (3390000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69c261a333123ee40938fa92f27b1d435e8ad7aad5212b89bebe490a613c636`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6bb051de3347c4d9049437be002ba818cd4f1d417ded7bd9faf3f2b6535baf`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13de9e382c27e5047737dfd2867d0d0cf0e8dd013f07c7be50b1e1a1dd800b37`  
		Last Modified: Thu, 04 Sep 2025 16:47:17 GMT  
		Size: 18.0 MB (18019443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721bf468705703556597d579c203b456cfe2722911b77c2d6b7903e4b8aae0a7`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:909cc8c4892e1607ffe7af2d231cb7e71effafc5a8752d267c0552e5f38bb0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07776a92b2e62dd43552588556afcba5e689d4f7e859ea02649abf7aa3d7845a`

```dockerfile
```

-	Layers:
	-	`sha256:2f02297fd46c6856422b935bcbcf389d235b7479989d9b858119d5a7f6275947`  
		Last Modified: Thu, 04 Sep 2025 17:08:01 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4-windowsservercore`

```console
$ docker pull docker@sha256:d310dcc104666bdc130f204f4b9d1fb7341508a9710b53a056e440710d60c667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28.4-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.4-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.4-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:875b4a57683b8cadc534c38b1a458b26f0ee03a02226ce29d1835369156f7bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:28.4-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.4-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:00efa870cb48d2587069580480eec0b1dbf1481faa14c899a74fc786b18562cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:28.4-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.4.0`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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

### `docker:28.4.0` - linux; amd64

```console
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4.0-alpine3.22`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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

### `docker:28.4.0-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4.0-cli`

```console
$ docker pull docker@sha256:0b928cff9f8f13b3475054da4af345db6b21007865f4fa3e0602b4422fea5f99
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

### `docker:28.4.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:73e41535043067691a7c87773c5185aa2d2bcf70da2770f878b1e31e13054980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76019659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056e2811a4634c5a0f25fe0954b56f24c25f926aeb1223b8952570b6c8713db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1bc58cae8b64023ff83a66e3e6c7a010244c2d0b37b31569b7410a3d0f160572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e4aa4c316414f5fda3df8b4df63fb46aa181d21ec0e7d5d2fd69b2b2a2deb9`

```dockerfile
```

-	Layers:
	-	`sha256:9949e013047bd65e547eba6bfd2cee9632caa48928b88b2cd515523f27aeb42b`  
		Last Modified: Thu, 04 Sep 2025 17:07:51 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad6e8b9bcb81416a9db3d34d65430e10e47acbcf37a4c9cf0db5c9a955a4e2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70947926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32618647e86987ce8f9b539cb4d3214f258794be577a61c143929f86609d52be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2421e5297d31e7232bf7c1ef83de638ab7a70e69240db127e82a42cc6255de18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1df48c0d35c4804846bf1c564dbdf23bbb014a90287637c98881ad47ad389c`

```dockerfile
```

-	Layers:
	-	`sha256:be8f9e60ee07824b3be12bd4898912592e94f0206efe05bbd40ca108856b2fc6`  
		Last Modified: Thu, 04 Sep 2025 17:07:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:36a89a541df1c76536798d2c70834c2a684fc40cd367da1991b38773b6687879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69940868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a8ff797b7c1f2e5c72cd2e8eb9736e52a036027dd8d9aac4ffb3a8fb99675b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6f52417beefc84301e134d1e6074194516b2daec77852e0c383b8c6cb8f3b6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcd14439dffea87510fd977e9a07dbfaf9bfcc03d46cb079c0459510051a3b`

```dockerfile
```

-	Layers:
	-	`sha256:442e4a644798d56efd70101e28ec5051f693ae9aa65ad0cb959bdac4c1ee77e7`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:124a8198af1cac6c30a13ea821f254b8699238d1c4d70212f689a2925b545233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71511020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb87a098f7d537ae39f72ab097a2a832e6ac09952042f6ee35eb0f760a16cc4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:90e3a9d1cb67f41875d2444f7b9cd67305425a82209e5debc8b0619d8b1c503b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386a491cf42f7a37851ceb04365b5fffec1b7efd6a6d0a3edb63fa41b885a63`

```dockerfile
```

-	Layers:
	-	`sha256:8ce75e56843ed96155ce89b112cae5e76e26f78cac99fea643694ce2aedc3459`  
		Last Modified: Thu, 04 Sep 2025 17:08:03 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4.0-cli-alpine3.22`

```console
$ docker pull docker@sha256:0b928cff9f8f13b3475054da4af345db6b21007865f4fa3e0602b4422fea5f99
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

### `docker:28.4.0-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:73e41535043067691a7c87773c5185aa2d2bcf70da2770f878b1e31e13054980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76019659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056e2811a4634c5a0f25fe0954b56f24c25f926aeb1223b8952570b6c8713db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:1bc58cae8b64023ff83a66e3e6c7a010244c2d0b37b31569b7410a3d0f160572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e4aa4c316414f5fda3df8b4df63fb46aa181d21ec0e7d5d2fd69b2b2a2deb9`

```dockerfile
```

-	Layers:
	-	`sha256:9949e013047bd65e547eba6bfd2cee9632caa48928b88b2cd515523f27aeb42b`  
		Last Modified: Thu, 04 Sep 2025 17:07:51 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad6e8b9bcb81416a9db3d34d65430e10e47acbcf37a4c9cf0db5c9a955a4e2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70947926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32618647e86987ce8f9b539cb4d3214f258794be577a61c143929f86609d52be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:2421e5297d31e7232bf7c1ef83de638ab7a70e69240db127e82a42cc6255de18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1df48c0d35c4804846bf1c564dbdf23bbb014a90287637c98881ad47ad389c`

```dockerfile
```

-	Layers:
	-	`sha256:be8f9e60ee07824b3be12bd4898912592e94f0206efe05bbd40ca108856b2fc6`  
		Last Modified: Thu, 04 Sep 2025 17:07:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:36a89a541df1c76536798d2c70834c2a684fc40cd367da1991b38773b6687879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69940868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a8ff797b7c1f2e5c72cd2e8eb9736e52a036027dd8d9aac4ffb3a8fb99675b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6f52417beefc84301e134d1e6074194516b2daec77852e0c383b8c6cb8f3b6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcd14439dffea87510fd977e9a07dbfaf9bfcc03d46cb079c0459510051a3b`

```dockerfile
```

-	Layers:
	-	`sha256:442e4a644798d56efd70101e28ec5051f693ae9aa65ad0cb959bdac4c1ee77e7`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:124a8198af1cac6c30a13ea821f254b8699238d1c4d70212f689a2925b545233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71511020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb87a098f7d537ae39f72ab097a2a832e6ac09952042f6ee35eb0f760a16cc4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:90e3a9d1cb67f41875d2444f7b9cd67305425a82209e5debc8b0619d8b1c503b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386a491cf42f7a37851ceb04365b5fffec1b7efd6a6d0a3edb63fa41b885a63`

```dockerfile
```

-	Layers:
	-	`sha256:8ce75e56843ed96155ce89b112cae5e76e26f78cac99fea643694ce2aedc3459`  
		Last Modified: Thu, 04 Sep 2025 17:08:03 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4.0-dind`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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

### `docker:28.4.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4.0-dind-alpine3.22`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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

### `docker:28.4.0-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4.0-dind-rootless`

```console
$ docker pull docker@sha256:4862cd916195b0e7a7823515ca74affdcbd259918bb393cae4480c8bf211a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.4.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3f6dd9dda95b8304f0d036045003a1ac2625d92a6d53abf88ebad522cce9ed34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169388498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e46e4df60bfaa2236d3fcb2933590c4331b5f66aacb86dd1a97cfd46e1cf59`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a220c8ec60c5c78af9d030015dbffc31df5f98bcb7ac9ed549068111713bd486`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 3.4 MB (3398455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdd74c6da8fedbd70ae176c68e2d0d3bf14c0f0ecca6859bb922b058cab0922`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b268299b4c1e90c236d9c1877cc2a56354da68eb7a9e6a06279c3f4d4ff32`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ede92035dcbd5985ddf6cada9ed6941caf4f53d763c83ab9e57f0c1eb8ee9c`  
		Last Modified: Thu, 04 Sep 2025 16:47:56 GMT  
		Size: 17.6 MB (17592033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2ec14a93ab2f5b33b5f9018640084359cea86ce9e2cedb1aa87187032d75f9`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6de2e74c4d99f16e038921cee84a89f66812e2a39c258d4d7ceb1be228d93ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5931ec4a77c8b88fbba7ebd8174da2c66e2819353e92d90f2782fe61832e56`

```dockerfile
```

-	Layers:
	-	`sha256:b863adb3de5876cea71f942b3f7285aa107d60c284402c23953e77dd172a8791`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.4.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d5e35da919bf42c0995a57696f671d0295d480843e1b5c20fac8f180cc48c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160766167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e05fa41c1eda1bed27053bbef7d3330dfc7e9105c90eb3d1fd24b2509a388bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131fba448ae92cbd556ec5ae35286e170ca8d311754dee6af2dfc86d1f65653a`  
		Last Modified: Thu, 04 Sep 2025 16:47:16 GMT  
		Size: 3.4 MB (3390000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69c261a333123ee40938fa92f27b1d435e8ad7aad5212b89bebe490a613c636`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6bb051de3347c4d9049437be002ba818cd4f1d417ded7bd9faf3f2b6535baf`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13de9e382c27e5047737dfd2867d0d0cf0e8dd013f07c7be50b1e1a1dd800b37`  
		Last Modified: Thu, 04 Sep 2025 16:47:17 GMT  
		Size: 18.0 MB (18019443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721bf468705703556597d579c203b456cfe2722911b77c2d6b7903e4b8aae0a7`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.4.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:909cc8c4892e1607ffe7af2d231cb7e71effafc5a8752d267c0552e5f38bb0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07776a92b2e62dd43552588556afcba5e689d4f7e859ea02649abf7aa3d7845a`

```dockerfile
```

-	Layers:
	-	`sha256:2f02297fd46c6856422b935bcbcf389d235b7479989d9b858119d5a7f6275947`  
		Last Modified: Thu, 04 Sep 2025 17:08:01 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.4.0-windowsservercore`

```console
$ docker pull docker@sha256:d310dcc104666bdc130f204f4b9d1fb7341508a9710b53a056e440710d60c667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28.4.0-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.4.0-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.4.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:875b4a57683b8cadc534c38b1a458b26f0ee03a02226ce29d1835369156f7bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:28.4.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.4.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:00efa870cb48d2587069580480eec0b1dbf1481faa14c899a74fc786b18562cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:28.4.0-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:0b928cff9f8f13b3475054da4af345db6b21007865f4fa3e0602b4422fea5f99
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
$ docker pull docker@sha256:73e41535043067691a7c87773c5185aa2d2bcf70da2770f878b1e31e13054980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76019659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056e2811a4634c5a0f25fe0954b56f24c25f926aeb1223b8952570b6c8713db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1bc58cae8b64023ff83a66e3e6c7a010244c2d0b37b31569b7410a3d0f160572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e4aa4c316414f5fda3df8b4df63fb46aa181d21ec0e7d5d2fd69b2b2a2deb9`

```dockerfile
```

-	Layers:
	-	`sha256:9949e013047bd65e547eba6bfd2cee9632caa48928b88b2cd515523f27aeb42b`  
		Last Modified: Thu, 04 Sep 2025 17:07:51 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad6e8b9bcb81416a9db3d34d65430e10e47acbcf37a4c9cf0db5c9a955a4e2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70947926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32618647e86987ce8f9b539cb4d3214f258794be577a61c143929f86609d52be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2421e5297d31e7232bf7c1ef83de638ab7a70e69240db127e82a42cc6255de18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1df48c0d35c4804846bf1c564dbdf23bbb014a90287637c98881ad47ad389c`

```dockerfile
```

-	Layers:
	-	`sha256:be8f9e60ee07824b3be12bd4898912592e94f0206efe05bbd40ca108856b2fc6`  
		Last Modified: Thu, 04 Sep 2025 17:07:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:36a89a541df1c76536798d2c70834c2a684fc40cd367da1991b38773b6687879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69940868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a8ff797b7c1f2e5c72cd2e8eb9736e52a036027dd8d9aac4ffb3a8fb99675b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6f52417beefc84301e134d1e6074194516b2daec77852e0c383b8c6cb8f3b6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcd14439dffea87510fd977e9a07dbfaf9bfcc03d46cb079c0459510051a3b`

```dockerfile
```

-	Layers:
	-	`sha256:442e4a644798d56efd70101e28ec5051f693ae9aa65ad0cb959bdac4c1ee77e7`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:124a8198af1cac6c30a13ea821f254b8699238d1c4d70212f689a2925b545233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71511020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb87a098f7d537ae39f72ab097a2a832e6ac09952042f6ee35eb0f760a16cc4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:90e3a9d1cb67f41875d2444f7b9cd67305425a82209e5debc8b0619d8b1c503b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386a491cf42f7a37851ceb04365b5fffec1b7efd6a6d0a3edb63fa41b885a63`

```dockerfile
```

-	Layers:
	-	`sha256:8ce75e56843ed96155ce89b112cae5e76e26f78cac99fea643694ce2aedc3459`  
		Last Modified: Thu, 04 Sep 2025 17:08:03 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:4862cd916195b0e7a7823515ca74affdcbd259918bb393cae4480c8bf211a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3f6dd9dda95b8304f0d036045003a1ac2625d92a6d53abf88ebad522cce9ed34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169388498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e46e4df60bfaa2236d3fcb2933590c4331b5f66aacb86dd1a97cfd46e1cf59`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a220c8ec60c5c78af9d030015dbffc31df5f98bcb7ac9ed549068111713bd486`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 3.4 MB (3398455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdd74c6da8fedbd70ae176c68e2d0d3bf14c0f0ecca6859bb922b058cab0922`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b268299b4c1e90c236d9c1877cc2a56354da68eb7a9e6a06279c3f4d4ff32`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ede92035dcbd5985ddf6cada9ed6941caf4f53d763c83ab9e57f0c1eb8ee9c`  
		Last Modified: Thu, 04 Sep 2025 16:47:56 GMT  
		Size: 17.6 MB (17592033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2ec14a93ab2f5b33b5f9018640084359cea86ce9e2cedb1aa87187032d75f9`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6de2e74c4d99f16e038921cee84a89f66812e2a39c258d4d7ceb1be228d93ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5931ec4a77c8b88fbba7ebd8174da2c66e2819353e92d90f2782fe61832e56`

```dockerfile
```

-	Layers:
	-	`sha256:b863adb3de5876cea71f942b3f7285aa107d60c284402c23953e77dd172a8791`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d5e35da919bf42c0995a57696f671d0295d480843e1b5c20fac8f180cc48c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160766167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e05fa41c1eda1bed27053bbef7d3330dfc7e9105c90eb3d1fd24b2509a388bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131fba448ae92cbd556ec5ae35286e170ca8d311754dee6af2dfc86d1f65653a`  
		Last Modified: Thu, 04 Sep 2025 16:47:16 GMT  
		Size: 3.4 MB (3390000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69c261a333123ee40938fa92f27b1d435e8ad7aad5212b89bebe490a613c636`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6bb051de3347c4d9049437be002ba818cd4f1d417ded7bd9faf3f2b6535baf`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13de9e382c27e5047737dfd2867d0d0cf0e8dd013f07c7be50b1e1a1dd800b37`  
		Last Modified: Thu, 04 Sep 2025 16:47:17 GMT  
		Size: 18.0 MB (18019443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721bf468705703556597d579c203b456cfe2722911b77c2d6b7903e4b8aae0a7`  
		Last Modified: Thu, 04 Sep 2025 16:47:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:909cc8c4892e1607ffe7af2d231cb7e71effafc5a8752d267c0552e5f38bb0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07776a92b2e62dd43552588556afcba5e689d4f7e859ea02649abf7aa3d7845a`

```dockerfile
```

-	Layers:
	-	`sha256:2f02297fd46c6856422b935bcbcf389d235b7479989d9b858119d5a7f6275947`  
		Last Modified: Thu, 04 Sep 2025 17:08:01 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:831644212c5bdd0b3362b5855c87b980ea39a83c9e9adcef2ce03eced99a737a
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
$ docker pull docker@sha256:25423ad06d7d86596d49a5af629ef9b2f1e4a049ffd09865e0b42396b6c38e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148396669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141d8d5b9ccb9bf761088a8576a1357c393dd70a8d85cae02cba797b3c59e69e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a5e87756b891f7c789cee62eb3bceb77fd284c0d2071863a9d1adafe23b249`  
		Last Modified: Thu, 04 Sep 2025 16:44:04 GMT  
		Size: 9.5 MB (9502525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168b20794b7ebd15f41f5c31b70080ba0d2dd90dd2fcffa54d6d1d112eb32a28`  
		Last Modified: Thu, 04 Sep 2025 16:44:06 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf7192c60d2b55938d3a9cdf3556bfdd5e32f71e5bf763c44c6158e3434cac`  
		Last Modified: Thu, 04 Sep 2025 16:44:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77166df98362298a6bf2d2cbf0997b4a04e3ce44e39c945857ab6551f4f68dac`  
		Last Modified: Thu, 04 Sep 2025 16:44:14 GMT  
		Size: 62.8 MB (62778262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478cc7997cbb94f495b889310cfe8888b0a56db3a0d17347061b945c94ac788c`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d3d9c6e5754de7e6053f91bd9cabd720fc05dc5e7025d96c19f9f49a38aeb`  
		Last Modified: Thu, 04 Sep 2025 16:44:08 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f92faa10e50f23065cf14e1e6ef889d7f501c16fb3b5cbb08266b63e80e9956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d768f2d4a3474ac22393a121de29fbda63fa2ede0e3e6aa94b8a300c8e081101`

```dockerfile
```

-	Layers:
	-	`sha256:d5c89e9a1b8cd8fe9a7ed90a49155b84f1acbc720b4e05067a67357461fb25e8`  
		Last Modified: Thu, 04 Sep 2025 17:07:35 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:3a7371bfbaa83e8bc8efdab60f61b81b5f731a079461ea506082b8ce7df10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139089052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887dcde88dcdf5389ca8302c0357eba3ba38647d78434b6f883851eb297f7aa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42ed802baf9fea6e93394dcf525233d26263cead3fcab4e5dc8773a2a1c8fcb`  
		Last Modified: Thu, 04 Sep 2025 16:43:47 GMT  
		Size: 9.5 MB (9461618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758b7b4bef1089860954115104c2226e81311bdf23ab9ec48746b4b74806c2d`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989f0c1298883619249969e4ef63ee7c56b55a39c84fe95cc5a8a4705cfb20f`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e409491ce29b81de94d50fbc9a8134051eb8c5febafddd3ea92a01eb07345bc`  
		Last Modified: Thu, 04 Sep 2025 16:43:53 GMT  
		Size: 58.6 MB (58583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f73798633f370eb4562e20129af69179ca80dcde50d71107650e2fcee8c47c`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4509549c80c438004b39bc300a0de83ce8095d33d71acaebabbdd3a05ce946`  
		Last Modified: Thu, 04 Sep 2025 16:43:46 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5f5feba194e7cc05835e1dbe825c6a0de2bdd289a58a846b7d10f79563e4da34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c840160a1439cb5d67dd7b9c614e96db6fa03598cf358bf6da45496d6d4a0d`

```dockerfile
```

-	Layers:
	-	`sha256:c75727c3763a160219d50550ae6f6b79c234e31f7d19b63b93952aedccc2ea42`  
		Last Modified: Thu, 04 Sep 2025 17:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:07e87ccd5c39a770feceb88f8353c065553353e4c87a9b647226d0e5027b1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137048141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbb7856a652103a04f14d7c598d9cf54d78f9fcf44e6c33f3b96d0a886bdb9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a51a130d7c2acdc4fd72676d9d59713454c04731eec3ce7a318b74d3834cce`  
		Last Modified: Thu, 04 Sep 2025 17:08:09 GMT  
		Size: 8.6 MB (8603169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ce063d6c70ce5d4066a34f00c8326c3e674bf2ec3a96a1f9b574b804ef81e5`  
		Last Modified: Thu, 04 Sep 2025 16:49:30 GMT  
		Size: 86.2 KB (86234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c771e41262119613794effecd75ee36ff660ea63b4fea3f37ba67c574e966db`  
		Last Modified: Thu, 04 Sep 2025 16:49:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eca08ed81d6271232544b1aef003ef8d561741af5459ca6f0bb00de8e8e9f6`  
		Last Modified: Thu, 04 Sep 2025 17:08:18 GMT  
		Size: 58.4 MB (58411866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f698dd04e72d5a1096763a8555dacd532e5d7f31d8779d7efe5bc5fe5cd454d9`  
		Last Modified: Thu, 04 Sep 2025 16:49:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc295d3a11822ae5fb6987034369c95c97fd20f5d805e8029509392ad62659`  
		Last Modified: Thu, 04 Sep 2025 16:49:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:2f9e822c0f9e83f2913ba7384807aab03494adc0b055c7fdc2e6e65112799e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0517bbeee436190aa12e90aa342cf69a04e5851d7b0b7994564190b62f280`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf8c81fdac51fd7928146c5a0147ba3989079ef2bc37ab36c56ea6577c9926`  
		Last Modified: Thu, 04 Sep 2025 17:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc2140f61e77be21b43859e6fd8d5134b0374f9231b888da2905e1bc32db4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139355382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680a0f55b2a2cc609608e6daf855c376b6db7f57eb3097247ecf0265fa89706`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7987680dc450799f14df53c67d78f2cc316e93c4e7a621261803ee505867d8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 10.0 MB (10031320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b142b52d842ca16848a3ea034ce49d6a3f576c8a340c9b4ace85f130f6724fa`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 99.3 KB (99311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d166701867aee943f4cab382a8dc6c7441349d3cee781b59f456f6da9c1a0d`  
		Last Modified: Thu, 04 Sep 2025 16:43:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c875db45b2e1d2690f059dfac173718f90a91051d6235bfd4e6754cb1c317`  
		Last Modified: Thu, 04 Sep 2025 16:43:35 GMT  
		Size: 57.7 MB (57707735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed319671941f08319fa1b31b6aeb6bbc0b56cf9086c69d9a4c63515ec44171f8`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f781b54762735409693c3e69969c74780e4ee02b4ed4f272dececf4d9462a3`  
		Last Modified: Thu, 04 Sep 2025 16:43:19 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:213ff489c13ef66be22c26b4dbd9f8c1906e7fb69f9bdfafd8f0eef1c3bef505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e414290fe34c1dc0030efb8947da2356ec95eeb1c43e17311c82c6298b8a29`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e25f4bb8fc0fe2b4e876209f7e3a770314a82078523122ac1b5d0002d4f63`  
		Last Modified: Thu, 04 Sep 2025 17:07:46 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:d310dcc104666bdc130f204f4b9d1fb7341508a9710b53a056e440710d60c667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:875b4a57683b8cadc534c38b1a458b26f0ee03a02226ce29d1835369156f7bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:00efa870cb48d2587069580480eec0b1dbf1481faa14c899a74fc786b18562cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
