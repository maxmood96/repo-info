<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.5`](#docker285)
-	[`docker:28.5-cli`](#docker285-cli)
-	[`docker:28.5-dind`](#docker285-dind)
-	[`docker:28.5-dind-rootless`](#docker285-dind-rootless)
-	[`docker:28.5-windowsservercore`](#docker285-windowsservercore)
-	[`docker:28.5-windowsservercore-ltsc2022`](#docker285-windowsservercore-ltsc2022)
-	[`docker:28.5-windowsservercore-ltsc2025`](#docker285-windowsservercore-ltsc2025)
-	[`docker:28.5.1`](#docker2851)
-	[`docker:28.5.1-alpine3.22`](#docker2851-alpine322)
-	[`docker:28.5.1-cli`](#docker2851-cli)
-	[`docker:28.5.1-cli-alpine3.22`](#docker2851-cli-alpine322)
-	[`docker:28.5.1-dind`](#docker2851-dind)
-	[`docker:28.5.1-dind-alpine3.22`](#docker2851-dind-alpine322)
-	[`docker:28.5.1-dind-rootless`](#docker2851-dind-rootless)
-	[`docker:28.5.1-windowsservercore`](#docker2851-windowsservercore)
-	[`docker:28.5.1-windowsservercore-ltsc2022`](#docker2851-windowsservercore-ltsc2022)
-	[`docker:28.5.1-windowsservercore-ltsc2025`](#docker2851-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:55e613fd4f85d921ce1ba31a1fbdab404fbf992c7ec7750940ad965102ece800
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
$ docker pull docker@sha256:113485a3795df8074a586ec560d7d83f02f45288904f30447610071c8c5eab72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318cd7ee2473ed74409c9c9e8e193689c609675aa0876a493396395e194f8d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e962273a03b1711fd22a2da1781c625fa33c2771b0a9c070d5878e8195f084a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f71ef9bacaaafc32f66e219a0d87f10600d5936b0552f89bd74fb233c64b5d4`

```dockerfile
```

-	Layers:
	-	`sha256:5566faad7ebda07d585cc6c3b7f99729e0021e8aac0ac59c21490b07638a98fc`  
		Last Modified: Thu, 09 Oct 2025 02:07:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:82202f05939bf78cd34db8fcc3e9a0f8dcd43810cf2d29b8f0e53029746509fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f6272d8aae7722421faaa78807cd2a841c47f007f6ed0732ef1bb05f6251d7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167047495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a24173edbd18315bcae77164bd0cf5c56a4868ec6c8c259fd3c6dbbce2d16a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a4ae80e5ee7a471d3efd0188e6ea3d561613a02d063f5250f4b3d678c82830`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 3.4 MB (3398365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b418b34aadf0cbb80baa73773f4f60426a8045bd08c25fcdc16ca7625bba24f`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889831ad97cef868cdc575a9ce91bf3d9a88ca19811addb324170bc68bd0cb03`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c556385820b127bafa4bb8c6a0f553a0821bcea18a2a2daa3ac8c9ad5b5149c`  
		Last Modified: Thu, 09 Oct 2025 00:13:27 GMT  
		Size: 17.6 MB (17593636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10586443f3a1c7e5f9004ca5aac42c2a7acd24f1d0812fe88061f1f7d30d68a8`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:64160a9f1d1ce1ac9b04faa3b6a79b714b87ea2dd33580dce38c4d19448489e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5547508af449ec639298e3c2e4f8405a3d7c970d324f86864d06025e5909ffd8`

```dockerfile
```

-	Layers:
	-	`sha256:9f5491c6522fada545d80bb1f9852fc8f338472f28d1833f42345231c5e46fe8`  
		Last Modified: Thu, 09 Oct 2025 02:07:50 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7b875165d0166ffa17e3909b979906abbf08082801483104518d17314f807016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (158042923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fccea9105ee3cc334f5020581fa663518ce5e6c894bd16642f9d7b81b2db39`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d9af89546d1ff37982ac36fa3856b48c100e5097b30d641657c49f40d2bea2`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 3.4 MB (3389922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001bb08497569fcd5703f8821da645ff794488c75a6a9e76bb9dea3da3f60a03`  
		Last Modified: Wed, 08 Oct 2025 23:22:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cc232eedf960a30d1b8aaabd74095eb6fbbf71254a7ba0112fa016d53bec17`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130f5d25803c36d5eb4a5aa833436b6ea9f43ac5428f24a944e8059bf91e705`  
		Last Modified: Wed, 08 Oct 2025 23:22:25 GMT  
		Size: 18.0 MB (18018146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc246780562d329f8918ad9248a22cdf5ed3ece527dc21436c3ed7041d7bc3e`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:87d6ad73f3450b2789a8bce22a4324ca08cd97521ffc2544e4a99a3d7902f1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cabc8e7b48765e75f07c637028ca144006ca1961985bb429f11b597406e5e5`

```dockerfile
```

-	Layers:
	-	`sha256:439a87135b5f853c8a1ee86ab008f1df20cb05a3b8e18797351a7b3119e7e443`  
		Last Modified: Thu, 09 Oct 2025 02:07:53 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:08fcf22b324f01b24d7d6c9edb2a077743fcb7a420e4263f0b1bca4952e41c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a850d0d3454900418bf8bd97acb002622a6ed5b1a77fa6fd76412b1f4f8ef768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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

### `docker:28.5` - linux; amd64

```console
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-cli`

```console
$ docker pull docker@sha256:55e613fd4f85d921ce1ba31a1fbdab404fbf992c7ec7750940ad965102ece800
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

### `docker:28.5-cli` - linux; amd64

```console
$ docker pull docker@sha256:113485a3795df8074a586ec560d7d83f02f45288904f30447610071c8c5eab72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318cd7ee2473ed74409c9c9e8e193689c609675aa0876a493396395e194f8d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e962273a03b1711fd22a2da1781c625fa33c2771b0a9c070d5878e8195f084a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f71ef9bacaaafc32f66e219a0d87f10600d5936b0552f89bd74fb233c64b5d4`

```dockerfile
```

-	Layers:
	-	`sha256:5566faad7ebda07d585cc6c3b7f99729e0021e8aac0ac59c21490b07638a98fc`  
		Last Modified: Thu, 09 Oct 2025 02:07:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-dind`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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

### `docker:28.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-dind-rootless`

```console
$ docker pull docker@sha256:82202f05939bf78cd34db8fcc3e9a0f8dcd43810cf2d29b8f0e53029746509fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f6272d8aae7722421faaa78807cd2a841c47f007f6ed0732ef1bb05f6251d7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167047495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a24173edbd18315bcae77164bd0cf5c56a4868ec6c8c259fd3c6dbbce2d16a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a4ae80e5ee7a471d3efd0188e6ea3d561613a02d063f5250f4b3d678c82830`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 3.4 MB (3398365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b418b34aadf0cbb80baa73773f4f60426a8045bd08c25fcdc16ca7625bba24f`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889831ad97cef868cdc575a9ce91bf3d9a88ca19811addb324170bc68bd0cb03`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c556385820b127bafa4bb8c6a0f553a0821bcea18a2a2daa3ac8c9ad5b5149c`  
		Last Modified: Thu, 09 Oct 2025 00:13:27 GMT  
		Size: 17.6 MB (17593636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10586443f3a1c7e5f9004ca5aac42c2a7acd24f1d0812fe88061f1f7d30d68a8`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:64160a9f1d1ce1ac9b04faa3b6a79b714b87ea2dd33580dce38c4d19448489e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5547508af449ec639298e3c2e4f8405a3d7c970d324f86864d06025e5909ffd8`

```dockerfile
```

-	Layers:
	-	`sha256:9f5491c6522fada545d80bb1f9852fc8f338472f28d1833f42345231c5e46fe8`  
		Last Modified: Thu, 09 Oct 2025 02:07:50 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7b875165d0166ffa17e3909b979906abbf08082801483104518d17314f807016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (158042923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fccea9105ee3cc334f5020581fa663518ce5e6c894bd16642f9d7b81b2db39`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d9af89546d1ff37982ac36fa3856b48c100e5097b30d641657c49f40d2bea2`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 3.4 MB (3389922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001bb08497569fcd5703f8821da645ff794488c75a6a9e76bb9dea3da3f60a03`  
		Last Modified: Wed, 08 Oct 2025 23:22:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cc232eedf960a30d1b8aaabd74095eb6fbbf71254a7ba0112fa016d53bec17`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130f5d25803c36d5eb4a5aa833436b6ea9f43ac5428f24a944e8059bf91e705`  
		Last Modified: Wed, 08 Oct 2025 23:22:25 GMT  
		Size: 18.0 MB (18018146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc246780562d329f8918ad9248a22cdf5ed3ece527dc21436c3ed7041d7bc3e`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:87d6ad73f3450b2789a8bce22a4324ca08cd97521ffc2544e4a99a3d7902f1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cabc8e7b48765e75f07c637028ca144006ca1961985bb429f11b597406e5e5`

```dockerfile
```

-	Layers:
	-	`sha256:439a87135b5f853c8a1ee86ab008f1df20cb05a3b8e18797351a7b3119e7e443`  
		Last Modified: Thu, 09 Oct 2025 02:07:53 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.5-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:08fcf22b324f01b24d7d6c9edb2a077743fcb7a420e4263f0b1bca4952e41c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a850d0d3454900418bf8bd97acb002622a6ed5b1a77fa6fd76412b1f4f8ef768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28.5-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.1`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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

### `docker:28.5.1` - linux; amd64

```console
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-alpine3.22`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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

### `docker:28.5.1-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-cli`

```console
$ docker pull docker@sha256:55e613fd4f85d921ce1ba31a1fbdab404fbf992c7ec7750940ad965102ece800
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

### `docker:28.5.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:113485a3795df8074a586ec560d7d83f02f45288904f30447610071c8c5eab72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318cd7ee2473ed74409c9c9e8e193689c609675aa0876a493396395e194f8d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e962273a03b1711fd22a2da1781c625fa33c2771b0a9c070d5878e8195f084a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f71ef9bacaaafc32f66e219a0d87f10600d5936b0552f89bd74fb233c64b5d4`

```dockerfile
```

-	Layers:
	-	`sha256:5566faad7ebda07d585cc6c3b7f99729e0021e8aac0ac59c21490b07638a98fc`  
		Last Modified: Thu, 09 Oct 2025 02:07:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-cli-alpine3.22`

```console
$ docker pull docker@sha256:55e613fd4f85d921ce1ba31a1fbdab404fbf992c7ec7750940ad965102ece800
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

### `docker:28.5.1-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:113485a3795df8074a586ec560d7d83f02f45288904f30447610071c8c5eab72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318cd7ee2473ed74409c9c9e8e193689c609675aa0876a493396395e194f8d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:e962273a03b1711fd22a2da1781c625fa33c2771b0a9c070d5878e8195f084a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f71ef9bacaaafc32f66e219a0d87f10600d5936b0552f89bd74fb233c64b5d4`

```dockerfile
```

-	Layers:
	-	`sha256:5566faad7ebda07d585cc6c3b7f99729e0021e8aac0ac59c21490b07638a98fc`  
		Last Modified: Thu, 09 Oct 2025 02:07:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-dind`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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

### `docker:28.5.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-dind-alpine3.22`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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

### `docker:28.5.1-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-dind-rootless`

```console
$ docker pull docker@sha256:82202f05939bf78cd34db8fcc3e9a0f8dcd43810cf2d29b8f0e53029746509fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.5.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f6272d8aae7722421faaa78807cd2a841c47f007f6ed0732ef1bb05f6251d7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167047495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a24173edbd18315bcae77164bd0cf5c56a4868ec6c8c259fd3c6dbbce2d16a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a4ae80e5ee7a471d3efd0188e6ea3d561613a02d063f5250f4b3d678c82830`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 3.4 MB (3398365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b418b34aadf0cbb80baa73773f4f60426a8045bd08c25fcdc16ca7625bba24f`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889831ad97cef868cdc575a9ce91bf3d9a88ca19811addb324170bc68bd0cb03`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c556385820b127bafa4bb8c6a0f553a0821bcea18a2a2daa3ac8c9ad5b5149c`  
		Last Modified: Thu, 09 Oct 2025 00:13:27 GMT  
		Size: 17.6 MB (17593636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10586443f3a1c7e5f9004ca5aac42c2a7acd24f1d0812fe88061f1f7d30d68a8`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:64160a9f1d1ce1ac9b04faa3b6a79b714b87ea2dd33580dce38c4d19448489e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5547508af449ec639298e3c2e4f8405a3d7c970d324f86864d06025e5909ffd8`

```dockerfile
```

-	Layers:
	-	`sha256:9f5491c6522fada545d80bb1f9852fc8f338472f28d1833f42345231c5e46fe8`  
		Last Modified: Thu, 09 Oct 2025 02:07:50 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7b875165d0166ffa17e3909b979906abbf08082801483104518d17314f807016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (158042923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fccea9105ee3cc334f5020581fa663518ce5e6c894bd16642f9d7b81b2db39`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d9af89546d1ff37982ac36fa3856b48c100e5097b30d641657c49f40d2bea2`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 3.4 MB (3389922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001bb08497569fcd5703f8821da645ff794488c75a6a9e76bb9dea3da3f60a03`  
		Last Modified: Wed, 08 Oct 2025 23:22:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cc232eedf960a30d1b8aaabd74095eb6fbbf71254a7ba0112fa016d53bec17`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130f5d25803c36d5eb4a5aa833436b6ea9f43ac5428f24a944e8059bf91e705`  
		Last Modified: Wed, 08 Oct 2025 23:22:25 GMT  
		Size: 18.0 MB (18018146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc246780562d329f8918ad9248a22cdf5ed3ece527dc21436c3ed7041d7bc3e`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.5.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:87d6ad73f3450b2789a8bce22a4324ca08cd97521ffc2544e4a99a3d7902f1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cabc8e7b48765e75f07c637028ca144006ca1961985bb429f11b597406e5e5`

```dockerfile
```

-	Layers:
	-	`sha256:439a87135b5f853c8a1ee86ab008f1df20cb05a3b8e18797351a7b3119e7e443`  
		Last Modified: Thu, 09 Oct 2025 02:07:53 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.1-windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5.1-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.5.1-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:08fcf22b324f01b24d7d6c9edb2a077743fcb7a420e4263f0b1bca4952e41c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a850d0d3454900418bf8bd97acb002622a6ed5b1a77fa6fd76412b1f4f8ef768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28.5.1-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:55e613fd4f85d921ce1ba31a1fbdab404fbf992c7ec7750940ad965102ece800
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
$ docker pull docker@sha256:113485a3795df8074a586ec560d7d83f02f45288904f30447610071c8c5eab72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318cd7ee2473ed74409c9c9e8e193689c609675aa0876a493396395e194f8d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e962273a03b1711fd22a2da1781c625fa33c2771b0a9c070d5878e8195f084a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f71ef9bacaaafc32f66e219a0d87f10600d5936b0552f89bd74fb233c64b5d4`

```dockerfile
```

-	Layers:
	-	`sha256:5566faad7ebda07d585cc6c3b7f99729e0021e8aac0ac59c21490b07638a98fc`  
		Last Modified: Thu, 09 Oct 2025 02:07:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ee987cd4ffdfcf157a4df2756fe649bcf28040e3120405621f2106d5b95a65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71167610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8797fa6025da5f6cf43e5c7d5a861a13c1310981b47c73deaf111403fc763d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:913a776a1640e30a4787299519798eece3065c0a11f093478d4fd2729f8d09f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb92b7516dfaf1ff47deaa4c43d8c5da5e5d5a3063009bcbfaca11b0f4638e`

```dockerfile
```

-	Layers:
	-	`sha256:c6429b41ec7e43b858d6fc47cfbdf63b75084dd78f7a456a4109e8ef5fa7d9ae`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ca49543195a1e53642ae43f301269504f6157911c85df2e1fe9a48f2b641a5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3864f57cedbc27d92173d6ce1ff98bd62deb24f2f012baa9bfd8c86bd18a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:27cfbd43240b2a36d9206e8d65ffa68cc828cc333dee94860ea8fe50fcdedc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54f87f9a325c1a28f3911b733bb8d436d5a344e5f4cab025423060c3122f12`

```dockerfile
```

-	Layers:
	-	`sha256:1c73b917de5769ed1585050836dd77eb606db44134e96525d7b6be3ce44aa0d5`  
		Last Modified: Wed, 08 Oct 2025 23:07:56 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a246a4a6c87424fc8e26fbd5f8f26e1ac19e2745da7e3c40be18b8c265ae1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71629206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9625f7aa2680d221b2ee306d6dd46be38d361c45cde6e47d84115ebc8faa619c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b2a82343ac247cca758d9a1cf13ec29c7705a3d4f11eac33840976a005f375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcf6dab5064a1fd34f33a9e7a5856d82a8f5ae4eb063493a494c9439eda61ad`

```dockerfile
```

-	Layers:
	-	`sha256:7879f0a2aa84744862fb9b29e3a5a4bcf9495ec25822e20b5e68e59056b15992`  
		Last Modified: Wed, 08 Oct 2025 23:07:59 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:82202f05939bf78cd34db8fcc3e9a0f8dcd43810cf2d29b8f0e53029746509fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f6272d8aae7722421faaa78807cd2a841c47f007f6ed0732ef1bb05f6251d7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167047495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a24173edbd18315bcae77164bd0cf5c56a4868ec6c8c259fd3c6dbbce2d16a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a4ae80e5ee7a471d3efd0188e6ea3d561613a02d063f5250f4b3d678c82830`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 3.4 MB (3398365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b418b34aadf0cbb80baa73773f4f60426a8045bd08c25fcdc16ca7625bba24f`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889831ad97cef868cdc575a9ce91bf3d9a88ca19811addb324170bc68bd0cb03`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c556385820b127bafa4bb8c6a0f553a0821bcea18a2a2daa3ac8c9ad5b5149c`  
		Last Modified: Thu, 09 Oct 2025 00:13:27 GMT  
		Size: 17.6 MB (17593636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10586443f3a1c7e5f9004ca5aac42c2a7acd24f1d0812fe88061f1f7d30d68a8`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:64160a9f1d1ce1ac9b04faa3b6a79b714b87ea2dd33580dce38c4d19448489e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5547508af449ec639298e3c2e4f8405a3d7c970d324f86864d06025e5909ffd8`

```dockerfile
```

-	Layers:
	-	`sha256:9f5491c6522fada545d80bb1f9852fc8f338472f28d1833f42345231c5e46fe8`  
		Last Modified: Thu, 09 Oct 2025 02:07:50 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7b875165d0166ffa17e3909b979906abbf08082801483104518d17314f807016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (158042923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fccea9105ee3cc334f5020581fa663518ce5e6c894bd16642f9d7b81b2db39`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d9af89546d1ff37982ac36fa3856b48c100e5097b30d641657c49f40d2bea2`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 3.4 MB (3389922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001bb08497569fcd5703f8821da645ff794488c75a6a9e76bb9dea3da3f60a03`  
		Last Modified: Wed, 08 Oct 2025 23:22:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cc232eedf960a30d1b8aaabd74095eb6fbbf71254a7ba0112fa016d53bec17`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130f5d25803c36d5eb4a5aa833436b6ea9f43ac5428f24a944e8059bf91e705`  
		Last Modified: Wed, 08 Oct 2025 23:22:25 GMT  
		Size: 18.0 MB (18018146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc246780562d329f8918ad9248a22cdf5ed3ece527dc21436c3ed7041d7bc3e`  
		Last Modified: Wed, 08 Oct 2025 23:22:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:87d6ad73f3450b2789a8bce22a4324ca08cd97521ffc2544e4a99a3d7902f1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cabc8e7b48765e75f07c637028ca144006ca1961985bb429f11b597406e5e5`

```dockerfile
```

-	Layers:
	-	`sha256:439a87135b5f853c8a1ee86ab008f1df20cb05a3b8e18797351a7b3119e7e443`  
		Last Modified: Thu, 09 Oct 2025 02:07:53 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:24173119fa6d1b5b4a27ab164fa7863deb66574ee5b90fef3b85dc888ef1a7e6
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
$ docker pull docker@sha256:7fd2c8237f6b295302d31c346b4532b9884e7bd53bf58235c4b8fdfc7ac3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e741a59d2b5a4679660c106679ebc7d4db788ddc56ff5e6741120cb5615ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ee3d4033409aab8a6343bd8f4946b63ed8ee6e592423bbe36b32cadd822eb`  
		Last Modified: Wed, 08 Oct 2025 22:32:10 GMT  
		Size: 8.2 MB (8205956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e5b145c180ee60a54e6e156baea080860d903bfcd11a832b670c45bea8a9d`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa9e8f5dad8914b50ad7caf05f3dcb2dd3189b83ec990d2c7cdfbb0171fefd0`  
		Last Modified: Wed, 08 Oct 2025 22:32:18 GMT  
		Size: 20.4 MB (20426222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17887135f865f0ab3373cb241459ebc39303e64585e5cadf2c8365f662a83a`  
		Last Modified: Wed, 08 Oct 2025 22:32:11 GMT  
		Size: 22.2 MB (22158437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0feeb7e94a43c4c8cda37dba49c4d214967b464377c9e588cc0eb8e712d822`  
		Last Modified: Wed, 08 Oct 2025 22:32:13 GMT  
		Size: 21.6 MB (21626205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1127a9962365d189931af70fc20c512713070321958dca0466f067f25455`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986754f3eee28eff01f2914dffa4e0bc1fe70af1029c708e69f0b8b274f7fde`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f2044987052c881ea71fb35249bb99d825b55d0fbb6fd287770d50acf6925`  
		Last Modified: Wed, 08 Oct 2025 22:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca549ef93bebd6ecb1ea9e1eb614278370b990827127716f2f500f654518617`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 6.9 MB (6905438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d213179b0c3ec131ebee2d3ff96c9aab5922cd4db88dec19519802affcda325`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 90.4 KB (90397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02593f0171881eb63346c54426f109e0d8732fdc381cd613aedf0ce2e34b020d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01c23d731ac1074e4613843aeb0a1af14c3bd930593c36ced366f92ba9389b`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 62.8 MB (62830891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bec682dd5602cd9980d04dca854f83d1ee95efcbcb9e98eb51413102d864c7`  
		Last Modified: Wed, 08 Oct 2025 23:33:05 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcdfe9ceca7df15d5ed8e966b67473cfd9878516b06cc199251ac3049e5392d`  
		Last Modified: Wed, 08 Oct 2025 23:33:04 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a72b359c0eff131fa8f3607be1f1f35b6440e9067ed43f1c256dafc17afec732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed64b844baee8bba095debaaa8a8ac6dcdd113cba6d88fcf71c6d045c591ca9`

```dockerfile
```

-	Layers:
	-	`sha256:a5780d59b7b2b80a499ed7c3463e3f7b9ced9d260d4a564ea54f15301b703fc2`  
		Last Modified: Thu, 09 Oct 2025 02:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:b2d48d3edc1b43bead3174514e241814e98a48231603633ef0ec3c438008c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137122808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae3788e80b9bc730d00170d72e7b43d8f27e57f747df4f01a570699266e6ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1557332ca1ff5d1254a6956972c84db8843fdf79b3b972d3ca2e555f25f070`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 8.1 MB (8113343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ba865655e686c70256ceb086f53e3d5a5a1c5d1f96a5ce983e70d4f1d71d7`  
		Last Modified: Wed, 08 Oct 2025 21:30:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9bc806622b42dc244a760b1296ddd201362ee4e575f8885a3d315d6f8a8d2`  
		Last Modified: Wed, 08 Oct 2025 21:30:08 GMT  
		Size: 18.4 MB (18418123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7934514c97217992015ceb73fdb3401ad1ff9a230a343bb1c251145edbe70e`  
		Last Modified: Wed, 08 Oct 2025 21:30:14 GMT  
		Size: 20.8 MB (20758334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4981d0ecc820d64501f656d51eedb9a723b61b7494fd7ab00081910c76d8c96`  
		Last Modified: Wed, 08 Oct 2025 21:30:07 GMT  
		Size: 20.4 MB (20371576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f4984fe9ee25ffb8ebb56de6f009860371a4f7ea1fd5bf71f5a71464847e74`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcdc987559659544c0494ab4a63591dbaab495619a255432e7624a9b9d2c43`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a9f9e5143a1dd352b4812c91e6545ebd4452cc085c93fa4a6d5adec62429e`  
		Last Modified: Wed, 08 Oct 2025 21:30:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c0f13664a55b1d62ca4fb496c22e96af8859c7de2c0edfc7aee77ca77d827`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 7.2 MB (7230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29df7ce9329c0b166d6eed8bd821f0c929cbe8df05f483b8c354d4a40f8d429`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 89.9 KB (89928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec834302b1af36e02e173b0e895b32004d96c310854731dd513e7e16c9059a4`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51230de100b143b8ab57448414a98ef6899e48594c31a7954d575b68bd1c9f`  
		Last Modified: Wed, 08 Oct 2025 22:56:41 GMT  
		Size: 58.6 MB (58629066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48887420ba80a8053bb99b2dfedcf6ff9e415cc8db662fb5453b3e68b59caf14`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363db79940c4b9ffbde6b8881cdacc6913c14a927b59e764c35db19fc11e29d`  
		Last Modified: Wed, 08 Oct 2025 22:56:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d52eea04fb331f4f3622e0282a8e29193958917d1412265d68858bd7081a2881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5821714912f95850da52086915d7384d19893b575c1ebc286803e12f9f8fcf40`

```dockerfile
```

-	Layers:
	-	`sha256:1a47832ff6d2676e6a189883e1127631c537aaf5cdcefab2dee8638c2e999565`  
		Last Modified: Thu, 09 Oct 2025 02:07:35 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:d8a4221f6ed1da9a5403e9108b2a5a96ca6712051f0d3697af8f01945aef4d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbd0482fa402511cada5526ce8d251597fc4f13a1f6f035a91a495f59b6fe0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906dd02debd48b1dffb412b1a790347448f2c3712ccbc82795e81504461280`  
		Last Modified: Wed, 08 Oct 2025 21:40:12 GMT  
		Size: 7.4 MB (7437530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed821fcb06f6348eecf28256465dbd580083f05e192bfa7e8f3eb7e7e28b52`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b714de4aad7d93f5fc356111498545e1157bba16bed035ae4d94b0630203e`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 18.4 MB (18402560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130ed747ce2f61840883fb7f4c22ca0250b3f6c0e1bcee1669054c73840078ad`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 20.7 MB (20744387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf56d5cdbb26c78fd221b2d6c89afc55bce44bd7c8a0cb0a7afee30e6f01421`  
		Last Modified: Wed, 08 Oct 2025 21:40:13 GMT  
		Size: 20.4 MB (20352522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6804fee98d9400cff95e3b40733b079cbb95efa641da7d5d13f07b5a92cd8`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1f13848b36edd043a9bab045a0575192e39f5fd8774d19df14c004458ecfb`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de40be23b483739798151e623d8021db2854de25ce98537bd3c5ad41e2241b9`  
		Last Modified: Wed, 08 Oct 2025 21:40:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f7f281e1132600c3e4f2577f68a1af9a4127a8a6ed99b87642b67a10f1b79`  
		Last Modified: Wed, 08 Oct 2025 23:14:23 GMT  
		Size: 6.5 MB (6538237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb20ceae03bc0a45aac594aa585d2178c9f9f803f881e2a098aa9d8f7ef5ccd`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 86.4 KB (86372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b821d0688742c45c98eea1aeec12595e695a218695a3256ca05553f750f728`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2585e076002e04cc2e1f19206b12ff6b5576fca0a8973f2b9bc993791bc84`  
		Last Modified: Wed, 08 Oct 2025 23:14:48 GMT  
		Size: 58.5 MB (58461602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6aed382b712a1fc8a97b966dbac8374acee156cd987b5556e5dd4260814e09`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031285e0952c0843f669ab2b48603662431b52faef93eb6fb39a337ad61ea0c9`  
		Last Modified: Wed, 08 Oct 2025 23:14:20 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6f158e10ebda484df9c1735b680d796bba723a45cafbeddd1ce129d3c134a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cbbf2f06140abf5867a57e358a4508226c0e4a9a1e7046df39c476d166c2`

```dockerfile
```

-	Layers:
	-	`sha256:0ce1a8efc890d0dffadd23ba89a1741588dc0a88f18ee1bd4f2228095a02f5e3`  
		Last Modified: Thu, 09 Oct 2025 02:07:38 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fa59ef1b10290d7760d2ff0fac47d56ef4469dd8278a8200e2d97f557e21a092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8315425933fa6bdaeef1a3b93620b0fd96a7bea882e7143379cc159797ea833`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-x86_64'; 			sha256='bd5835ccbbf06a42dcb5294c65e34a4634b34447afb9ed6fc7adf18a000e0f99'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv6'; 			sha256='458294be13e0619118692aec3b6374e70c83d0dfcf16ae59437f349b64021948'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-armv7'; 			sha256='12f853e0cbf02a069f01a5f41e3803815b6f7ae3a7574d6f792c8de36f1b7bfa'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-aarch64'; 			sha256='fa99ca94c96c8cae4024493581a20049764ce723558991d0d1526c1c7b791a79'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-ppc64le'; 			sha256='aec0a582aeafec11a77c8b866e3d5ae42872a33bf457520a4bfc8436a96327d0'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-riscv64'; 			sha256='5f9778000b556c2240942e95b61b24834d9f46f52ac294c5ea0d22f187fbde48'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-linux-s390x'; 			sha256='2642108b41b19fe48e777632ed0def6289b14a054f427ac54b6130d7f95b9909'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Oct 2025 16:45:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD ["sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 08 Oct 2025 16:45:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:45:42 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Oct 2025 16:45:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Oct 2025 16:45:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Oct 2025 16:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e005d6027c0fa85d63fe786637ba67e700d5d4fd9722c84a4d72f75b2251f`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 8.2 MB (8227554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0ed7ca0caa517ef5238ba991dc3e4220463e02973947da2237b01188acb44`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02cf21bdcbda98b8d8d8370c5bfb37ab7306d988222873e48a1eb09330cd4d`  
		Last Modified: Wed, 08 Oct 2025 22:31:08 GMT  
		Size: 19.2 MB (19232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6658d6a7fd639e07ddb72d3af42f988868f7017b5bb1524f54dd87c3bf5a1`  
		Last Modified: Wed, 08 Oct 2025 22:31:09 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff55b330560ea33000aa48ed2ff42a414ca04bf2b67d5bf5e3059f032e37588`  
		Last Modified: Wed, 08 Oct 2025 22:31:10 GMT  
		Size: 19.8 MB (19755370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775250c0ba12aa5e1a82909288e783df98154d1fdb73b0ac77bb29e82f185b7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a2b2ed6b558e680bbc59d1a9fd1cdba32f3e2e6740adf8d2ee0950402475b`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88257e397f43129543a2706c97fb8be853592242bb816d8087c23c1ef7246f7`  
		Last Modified: Wed, 08 Oct 2025 22:19:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac41ca9a2bd1609e402f70367074366b4d885c9ee55d45af72b724ea078a6a`  
		Last Modified: Wed, 08 Oct 2025 22:51:29 GMT  
		Size: 7.1 MB (7140783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30218bbe623e6ce34b91a3a892c8cbf139b6bb79a8fd99ea8d38f3a33ba70392`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbb1ea2f3f1292a013205d9489a868130739ab51d47c8997ae44ea10150cf6`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee62bf560b751730e33758916b902b1c6d60f162d60c9867607d84e6f28a95f`  
		Last Modified: Wed, 08 Oct 2025 22:51:45 GMT  
		Size: 57.8 MB (57758046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785720463b465736227e54bb866f7192d63decad868451fc887f12f20950d61c`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39b23fc1b31d943bfe1397c6d089f8a915a3ad8e4a5d5c11d6d4de52905824`  
		Last Modified: Wed, 08 Oct 2025 22:51:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f889211464e1bca6cdefd904238c55643bbefad60ae5675e93f72077a9c0587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb74d8a6ad2f8eeb7bb5c4be09c35333093b756a85e276d4f22b76c48517cb`

```dockerfile
```

-	Layers:
	-	`sha256:82a75aedd003fdd9725852e775183f1ce60f777141333cc11f842aafe20019e6`  
		Last Modified: Thu, 09 Oct 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:337c819e1e92bbe665964fa9ff8420a91cd889d8b99ba336749af5eb20bd5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:08fcf22b324f01b24d7d6c9edb2a077743fcb7a420e4263f0b1bca4952e41c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:e56c170808ca78c26deb0498a3b5600916f30b52e02e4cbcad48e4e5413bac2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349063868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1531e0c5fbf62b45088caeba2a3ea3dffeb024dc05b6171c7c58ac6bedd7752`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:36 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:25:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:25:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:25:02 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:25:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d236ee3ddb494a43777cf4c750e11f24a6855d4f014aef887d9bb3eb8cec65`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 375.6 KB (375593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2b2a13e8d766d7112787c3e566cc24861876650129e0fa646ea94861657a80`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1456bbc414c1f59bc11adbbfcbff81e1fa79e1dfcd25b9145b5721982f836a`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157da88bcfea69925be36eb4eba1f5ae892676f38b02e34a7163952ce88152a2`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 20.8 MB (20790415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c7bdab2be09c68de1a125a229d086cfc49bc31c636dc9fc973d03b0a35de46`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca9801d79367ec64b91bc31eaa6d4d94484105ee4ff6e202e05d6cdd2eae62b`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2a38cea6049ba28b1b50734f7e550cbb7f0e91900e96c8c0d18b93141da872`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137838ae62da239ca8112ae8926c948302590c5f77bdee4fc44c9c1d94b144b`  
		Last Modified: Wed, 08 Oct 2025 20:26:14 GMT  
		Size: 23.2 MB (23171440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d773f22147b59b34d1a347ff85a839862597d1e77b11a787659b2f04c2de0f03`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641ca824be3a966de4c18426c4f8f6b885e357996cb55411596e8f1032d6509`  
		Last Modified: Wed, 08 Oct 2025 20:26:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c15da681c6f87e9982d18ba1de5ce9721a37f95820a8a4800db264bf5a8c23`  
		Last Modified: Wed, 08 Oct 2025 20:26:05 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd59d774caefda6512e700264edc21f7745671fcd4ee62d32e58a577744f86f`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 22.6 MB (22569661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a850d0d3454900418bf8bd97acb002622a6ed5b1a77fa6fd76412b1f4f8ef768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:456608367ee981baab950276c7b716bdc284572754e2b76c142d79819287cc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638415153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de142641f3d8bb4cfea6e08c7c95aa0e9103fc9a905b20eb571aa0ce5654fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:23:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 08 Oct 2025 20:24:09 GMT
ENV DOCKER_VERSION=28.5.1
# Wed, 08 Oct 2025 20:24:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Wed, 08 Oct 2025 20:24:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:23 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Wed, 08 Oct 2025 20:24:24 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Wed, 08 Oct 2025 20:24:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 08 Oct 2025 20:24:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Wed, 08 Oct 2025 20:24:35 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Wed, 08 Oct 2025 20:24:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd546668718edfe8745f1d5429759c685e77264089ca55ecd7800a89f20b85a`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ae5737af16929a35531b7b689896466df87f227a31056d1ffaa5c70c2583f`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 396.5 KB (396460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cb21e92bbcb5dc753299aa7c8342f00535ec4b3f25ab1cd9f6c691efcfcf5`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae86c53cb3e217c9d9742f1c8e806844b46f78ab061f5a357af0af70f7758cc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9093fd1eb9803e1e6e56c4641b28b80a101f8b5f6c8d1d56e426f0b37007a7`  
		Last Modified: Wed, 08 Oct 2025 20:25:22 GMT  
		Size: 20.8 MB (20803086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ca09c60fe50cfd23dba8d4c605974633b3435281df3b32ae07571f63c5a36`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40f24005e5ebb802637dd1e1311783ef691fbae4a2b5d75149db686e18c47fc`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb1fedcc42ddc959dfcb0f41c07edfcbbd614d5e9d14244b4a7916693fc451`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3a566b8b37776d50ca23f62478277ec62b2b6f91217c1b012e9780bb32cd`  
		Last Modified: Wed, 08 Oct 2025 20:25:23 GMT  
		Size: 23.2 MB (23183118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b763b1988b08dcae33159058102e0db6df0752953000232df6732e5cf2bdd32`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86a99257a476810c7c900d936f1fa4cddfba2d9409237f74b2813dfb45bbe0e`  
		Last Modified: Wed, 08 Oct 2025 20:25:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be601b3316d7cc0822704ed497a4e912ea959df47eac981dbe2662be7f2a228`  
		Last Modified: Wed, 08 Oct 2025 20:25:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577172842fa01db6f3bc2f8f54f393f4e622f4bc0fd0efaaa132449191ee633`  
		Last Modified: Wed, 08 Oct 2025 20:25:20 GMT  
		Size: 22.6 MB (22580892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
