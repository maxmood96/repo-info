<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.4`](#docker274)
-	[`docker:27.4-cli`](#docker274-cli)
-	[`docker:27.4-dind`](#docker274-dind)
-	[`docker:27.4-dind-rootless`](#docker274-dind-rootless)
-	[`docker:27.4-windowsservercore`](#docker274-windowsservercore)
-	[`docker:27.4-windowsservercore-1809`](#docker274-windowsservercore-1809)
-	[`docker:27.4-windowsservercore-ltsc2022`](#docker274-windowsservercore-ltsc2022)
-	[`docker:27.4.1`](#docker2741)
-	[`docker:27.4.1-alpine3.21`](#docker2741-alpine321)
-	[`docker:27.4.1-cli`](#docker2741-cli)
-	[`docker:27.4.1-cli-alpine3.21`](#docker2741-cli-alpine321)
-	[`docker:27.4.1-dind`](#docker2741-dind)
-	[`docker:27.4.1-dind-alpine3.21`](#docker2741-dind-alpine321)
-	[`docker:27.4.1-dind-rootless`](#docker2741-dind-rootless)
-	[`docker:27.4.1-windowsservercore`](#docker2741-windowsservercore)
-	[`docker:27.4.1-windowsservercore-1809`](#docker2741-windowsservercore-1809)
-	[`docker:27.4.1-windowsservercore-ltsc2022`](#docker2741-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:b0c1179ea32ad77bdb7b852b037e54b11022304c2f2662af1954ef53869314b2
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

### `docker:27` - linux; amd64

```console
$ docker pull docker@sha256:30564d91cacde37f23816c72f6f86a2d02cbe19d681af326204dce73aee3117a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133445714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8314b971e611487bd98e2907c84df89c10243359ecf1452511dfa5cf594659fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:c96c9e5fbcf5f8d775e51157e7dba70c5e097eceb7426fee07d1bd3b0ac3a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058db2570bc3a5e6ac3238878cfc59aa2ecce3aa0b7f01037f9b5744669d9fbc`

```dockerfile
```

-	Layers:
	-	`sha256:bf8e28afb515352bee40ed5d10c10c5be26f8d887c3e7dcdb88dba5cba602f98`  
		Last Modified: Sat, 14 Dec 2024 02:09:01 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:da6c6379c896b324b06a60ee4a59b170cead5db69a611d58a4a4de4c4c11d306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab07ed540216bdc6189cc7d618da391102c16a16effab1b13dd9bc6eda0f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9b0c55946c0072f1e907f3ee32335a36486a3cd05e42d4e77d30bf8216579f`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 7.0 MB (7037847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d10f548f19c5bba979fcb569834d58e76aff1660a01a0aaf60c9a4a37ca225e`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 89.0 KB (89037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de881962034d29a659cf033f217cf53f013b7f4450e93b99e924b9be583c0d8`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52fc45c7376ba4b93b55bffffddd9b23f5576f74345b1807dbc8f31d852f4a`  
		Last Modified: Sat, 14 Dec 2024 02:08:33 GMT  
		Size: 53.8 MB (53836527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94314352676036e11c60b0e8444d38a745cc65bf67e2c8ed7c05ed9703f28c6b`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16244b8e1e1833788b525bf083eaed44b06a0cd84890a61ac5c17ee22ca6bb27`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:a28c353d7c6268dbd78f696ab407329a648ce9b2f7e6d208cc0d81501074fcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c52c05056c0632f86e19f6a07ac6dc323f1f405842cb23a46ebf061095afd28`

```dockerfile
```

-	Layers:
	-	`sha256:10f600e291d01a48cdd062ee030d72c4bf5a329c0e2df55014c65b161f782ccb`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:7476bf2ec4f13b8681c236b2b26169a5e5a1b3e3067584f5e8f19063f14ab7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122917849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e6717a522d6e5aabe64ab82c5b1fc8b1da3379d43d357f92a6bc13c149f79`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1aaa6f59bd8bea60c22455fb321ddd89ec0b16a6624e1e281e196f100272e`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 6.4 MB (6364981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f179410e55cf07e54cab8edce1e06e30c1dc5cb148acc3674c9c0ecbccc12290`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 85.2 KB (85194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc7ae7d0eef0f8bc25ca2dd6abb99c77404da8155f8f534272a25e7c019722`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b7ae134b8d5df6f3f9c0ad02de62cd38404cbc6c3e675552b0541d3285b1d`  
		Last Modified: Sat, 14 Dec 2024 02:17:21 GMT  
		Size: 53.8 MB (53836568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9884ff30eb5303229cbe20675efa4ca532465af5f9dd1a202dce1db5eeae9410`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9e60dcacfa37d04df6b41f0040e3ff9f4f0a98da2bbee6626e04d41824f0e`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:e72cfc40e2a8d6bf2750810862d97a7f8c726a6452405cc30b228325bba2049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e257ba2a900b3722edec07c23b17c8836263c690a781f8754f279c11f3ecea1`

```dockerfile
```

-	Layers:
	-	`sha256:60187e854ca504ec911ae6ac416045a534aec8e7ecf7eb54c3c7d66cf0717f70`  
		Last Modified: Sat, 14 Dec 2024 02:17:18 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:354a62c65fcc5fc052ae7ec2eeee6e556f4fe18fe50eb16e4de9e8e765d6e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125252835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5bf689786a37b6f8dde9e6892fe3e0a3285f204f206b635ab597c8fea8cfa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:9b8296cb2db780e6832b39b3e00ee55a8e7797948cd9db9406d948c5cae7a859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0f8db20f775e9edfdb0877cea59a0382cbd87e0ce9ea93717d4088b44fbab`

```dockerfile
```

-	Layers:
	-	`sha256:1c4131432fb5fbd9f96d2130052881001fe65a6a0de6cd98d64efcb94f184edf`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:561338cb111f09a755c9c28e00b66a2466a3dacd88bca6f2f0aeaf909e95730a
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

### `docker:27-cli` - linux; amd64

```console
$ docker pull docker@sha256:167c735d631b00384e268f1dd1230ada3bdcac915e749be562481fc37d7cf5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68472707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37409751f89a9183b99563f929bf21325fa6cfcf287679826ec502c1202c3ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:30ad0a07ac64a65ddcd433aeab8a1e559fa50327cb85fa12c22c6b26bdf8763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d0aa13057ebc4ae8e2594681075d7484b2d6e2aa8f0972640a33edf65f20fa`

```dockerfile
```

-	Layers:
	-	`sha256:87259a40baf16e0ae65ac41ce9f8eec992f0fec996d1f945f3c11306b74847e1`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:850519e09ac90396d48c2260b38db241f84f74acb4d372f03ae988d8b1419014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63604936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7f1cecb9a3b1e66edb8ea720a313bd0d7ad69900fee316c2b572c0b2464e12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2d2e4a9727681cfe5637fed05f28442cfeb4e3d4c74b54d1666deea18dbb2f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbfe47a312b92570b77592a48ed008e485b15bb45396495a529a8a455775092`

```dockerfile
```

-	Layers:
	-	`sha256:a14543e98fa59723762ef528b045c1706dfa299cb0a2db5d3c0c940e7ab6e645`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4b6e4baf1ab15df1260382122b976234e24237558bc65513671571609a18bc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0518d1dd421d96cd8f33089a34770da57b68c2740d3b9523f761895f742ed317`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7cdeed720491a6c79999649859d8812011a8a80f99517f4940721f3b106ce4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7cd806863913b1082373e133d60b368631c92a06b92de0243c5876387a0a79`

```dockerfile
```

-	Layers:
	-	`sha256:843f0814593e40fbce871757fbea33ed8b9899f195a215342068a202ad2e0ed3`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a73907930d8ea382a8bfacc5362eb0640cb90f7416b75e42c24bb018694c19dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64440237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71be0f3c62209a33bbb2557f941d3e6e819568152fb39d16dba4e50fa13c6f14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4089d1cdec8b176b873a1d1e877c8bae7d65f093b06b8fbfe1d3e96d0a10cfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e62058998eb61300889bd4e4372fdfce6cc78bde26e2baaa436fcb4b10b0863`

```dockerfile
```

-	Layers:
	-	`sha256:93a1a3e41ef910ab186cf149424caadafef5cf4a7c34e68f789ab980b0483245`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:b0c1179ea32ad77bdb7b852b037e54b11022304c2f2662af1954ef53869314b2
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

### `docker:27-dind` - linux; amd64

```console
$ docker pull docker@sha256:30564d91cacde37f23816c72f6f86a2d02cbe19d681af326204dce73aee3117a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133445714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8314b971e611487bd98e2907c84df89c10243359ecf1452511dfa5cf594659fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c96c9e5fbcf5f8d775e51157e7dba70c5e097eceb7426fee07d1bd3b0ac3a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058db2570bc3a5e6ac3238878cfc59aa2ecce3aa0b7f01037f9b5744669d9fbc`

```dockerfile
```

-	Layers:
	-	`sha256:bf8e28afb515352bee40ed5d10c10c5be26f8d887c3e7dcdb88dba5cba602f98`  
		Last Modified: Sat, 14 Dec 2024 02:09:01 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:da6c6379c896b324b06a60ee4a59b170cead5db69a611d58a4a4de4c4c11d306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab07ed540216bdc6189cc7d618da391102c16a16effab1b13dd9bc6eda0f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9b0c55946c0072f1e907f3ee32335a36486a3cd05e42d4e77d30bf8216579f`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 7.0 MB (7037847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d10f548f19c5bba979fcb569834d58e76aff1660a01a0aaf60c9a4a37ca225e`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 89.0 KB (89037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de881962034d29a659cf033f217cf53f013b7f4450e93b99e924b9be583c0d8`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52fc45c7376ba4b93b55bffffddd9b23f5576f74345b1807dbc8f31d852f4a`  
		Last Modified: Sat, 14 Dec 2024 02:08:33 GMT  
		Size: 53.8 MB (53836527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94314352676036e11c60b0e8444d38a745cc65bf67e2c8ed7c05ed9703f28c6b`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16244b8e1e1833788b525bf083eaed44b06a0cd84890a61ac5c17ee22ca6bb27`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a28c353d7c6268dbd78f696ab407329a648ce9b2f7e6d208cc0d81501074fcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c52c05056c0632f86e19f6a07ac6dc323f1f405842cb23a46ebf061095afd28`

```dockerfile
```

-	Layers:
	-	`sha256:10f600e291d01a48cdd062ee030d72c4bf5a329c0e2df55014c65b161f782ccb`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7476bf2ec4f13b8681c236b2b26169a5e5a1b3e3067584f5e8f19063f14ab7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122917849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e6717a522d6e5aabe64ab82c5b1fc8b1da3379d43d357f92a6bc13c149f79`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1aaa6f59bd8bea60c22455fb321ddd89ec0b16a6624e1e281e196f100272e`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 6.4 MB (6364981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f179410e55cf07e54cab8edce1e06e30c1dc5cb148acc3674c9c0ecbccc12290`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 85.2 KB (85194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc7ae7d0eef0f8bc25ca2dd6abb99c77404da8155f8f534272a25e7c019722`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b7ae134b8d5df6f3f9c0ad02de62cd38404cbc6c3e675552b0541d3285b1d`  
		Last Modified: Sat, 14 Dec 2024 02:17:21 GMT  
		Size: 53.8 MB (53836568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9884ff30eb5303229cbe20675efa4ca532465af5f9dd1a202dce1db5eeae9410`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9e60dcacfa37d04df6b41f0040e3ff9f4f0a98da2bbee6626e04d41824f0e`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e72cfc40e2a8d6bf2750810862d97a7f8c726a6452405cc30b228325bba2049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e257ba2a900b3722edec07c23b17c8836263c690a781f8754f279c11f3ecea1`

```dockerfile
```

-	Layers:
	-	`sha256:60187e854ca504ec911ae6ac416045a534aec8e7ecf7eb54c3c7d66cf0717f70`  
		Last Modified: Sat, 14 Dec 2024 02:17:18 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:354a62c65fcc5fc052ae7ec2eeee6e556f4fe18fe50eb16e4de9e8e765d6e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125252835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5bf689786a37b6f8dde9e6892fe3e0a3285f204f206b635ab597c8fea8cfa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9b8296cb2db780e6832b39b3e00ee55a8e7797948cd9db9406d948c5cae7a859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0f8db20f775e9edfdb0877cea59a0382cbd87e0ce9ea93717d4088b44fbab`

```dockerfile
```

-	Layers:
	-	`sha256:1c4131432fb5fbd9f96d2130052881001fe65a6a0de6cd98d64efcb94f184edf`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:5b6982daa87eac334c19156bfbcaa7931ac5758857d951b05be6136184534394
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:fc55380e4b93f80c1ed6d12d49cc548099c2cf4fc463a40d2e45a7441a15d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155737519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8322a7c3c8154f09895c7509500e24519267dec8b762f4d2243bd47bfefd97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e959b26a34438101745b4a6b12e2158e837753abb318a703d6a997acee940b32`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 986.6 KB (986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c29d0936b41295dfa648ee92b27ebca2e18c10700ce27472e57dfdbcec4c6a`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d19b2a60bc8d264042588663e4e123d26cbedf4aa96bbcf6ca5483bc82ca2`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50381dd0e19aea2b08429ae4b5824848b0e9e42926ee71822ae02df5e2693d16`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 21.3 MB (21303866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653b8fb52f49b277b1595dfbe1e5b2c3689df958d2df014003ce5cba5b7aa0c7`  
		Last Modified: Sat, 14 Dec 2024 03:07:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f6e358577a60d964b0f1b11ecf89a63cb21351522e15f87d7dfc6ebcda5969ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28cc68cd831df9a34e164fc2ea5b3f364ee6b02cc1f49f036ca59a72bc72571`

```dockerfile
```

-	Layers:
	-	`sha256:644bc1fff97fcf26268d33246cca53014486994146f0e5d4b02de3f5a26c9bcc`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47cd9b46cc39d1ea39ce702f2b197f78006e12d471ac0d9143046b0805d3880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149423499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486e46f1028dafc6440042fcd3a8a6bb5cefda114320b24a99730bc21b9f2484`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1095688739528f200fadd7670e4c7b354566e5b6a5663acc8690e24430f6e3`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.0 MB (1014153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecbf2c620964818ee2dcbc20a175aad27a6fb8b052fb19dd701cbbdb6f23e78`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac17c515dbd19f47019153943183a2995ace4060877f16ef7a715db68ae4181`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8818bf23aa3c08119351a436f05fc62b25a1fa448a59f02e05804a5ab92f00`  
		Last Modified: Sat, 14 Dec 2024 03:07:29 GMT  
		Size: 23.2 MB (23155158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056092e1c446a0219de668b0289797f8369a23417dd278d159af0606bf9b74c5`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f695216a693f4d4041900f72c45a3e39ab19ae5c1727df82414c0e158a605ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c5773897944ec73002da42dd7bafb32c8788aadf785e3ffbd20df78b3d7de2`

```dockerfile
```

-	Layers:
	-	`sha256:732f97201f7324ad6916ceab73e27ea9cf755fc3a41522c77793bdef203efd55`  
		Last Modified: Sat, 14 Dec 2024 03:07:27 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:533317eb15b02dcd3b6ce9594eb64b19fbb8d5d885addfe2535284535aafcdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:4c61e196683cde572c15fca7d82ec0144d9baf103fc6efb3ae6b0286edd22229
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0c061d2dfcfe6fe2ce770d0b408089cf231775768271407f41c74838440c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 14 Dec 2024 01:28:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:30:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:30:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:30:49 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:30:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf35bbd2931d5fbc55601ef6e88a070c1c0fcc111ab88d99f23348e6cf3a0045`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1808d92f4b99551366b64eae9a9325635d4682408682362e6937d29f5f13db5b`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 357.7 KB (357749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d251f59aac7a5e6567afa4b6afd184f856799c714cda863faddfaf90c90913`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a50f99fd0a08f9d021d34918b3da7a628eb525bcfcfb2a1a1f8c8505f75a37`  
		Last Modified: Sat, 14 Dec 2024 01:31:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310fe7a9d7f781c68c95bb89feff0c0df181313bab50354edffe3ac98fcde4a`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 19.0 MB (18964823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4caff6cb48bd16bcfa5b4883d1b28f4754027b31ec5a130b033f3eb60076018`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d30bfe873c38caa89e51f0346cd5ac3ac398ba811bd23a40b96cb0a371f573`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f185c99ce4f1ffbe43c348be2f1bc873d95393a9c41e5ef71b56efe7d7c39e01`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c0a2d297f342b497a6e32ae77af4ae9310c57d0c28ce7df8100789b50298d2`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 19.6 MB (19615541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e883c865c34857d45a00cf0c21a4565103d0affaf23f50cd7fc717e51e8c5e`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc1a70b9c7b9b3bb4473f12cdf6b227941556b863bea1b52a1a9e7d0d30ebe`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6eaa117645bb79a6c99d1c87cef7a299e6646ea5b44d4252e46259a303c0c8`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2e4fd1f921a57729068da3fb938e48bd7965db83068ceba6e3729c8954d`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 20.1 MB (20133275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:8ef8875f2aea79b08c8efa7cd5178a6d9b9593713f40c34cf6ad86e27f799267
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073463613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff54bafe6449abc1b00e591cb11ef385a94d4f4c2a1ef229cd503e0af951d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 14 Dec 2024 01:28:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:58 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:31:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:31:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4bbf7603280e18fef610d62bb0c1efe65eac0d049e0ccbb9c0bb08f368b44`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1294661f7b7b87018d8fb44eb2efa68eec9eb81314c718a493674d32b060b0`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 475.7 KB (475685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d76bd2d48b330e49e4e81c438687e39d7c5fe09bd979da61260f4112a4d7b8`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038de22c9679725e51fb20c3737057ff9ad931bc0725ba5ff42828cd86326f1`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75493ded187a3dc441832ca8c83024487f65272e109da46e3694c0675dc48462`  
		Last Modified: Sat, 14 Dec 2024 01:31:30 GMT  
		Size: 19.0 MB (18998230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9582b154c37509bd6fa7478d4cd602ec5ed1619bd60431de73b99651a2f648`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062405b264d614c41ced78855204ef55a53ddc2103621c8be0f22b4aaff6a0`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d88c5fc0cf0bff6bebbf6f1657990d2898dc69cc5797ebf8e2f656ead725`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833c72764532458c8b7b59609cf6ea55f422a04d6106d24db935ca247026e1f9`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 19.6 MB (19648271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea4c7b5bce6b6df9d1d3810806051f1c595893855de8ce49f45f74ee9341916`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ec6e556fcb04398b6dd8f733bc38bb2bca5be00bfda9edb57e46c3bf8d9410`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf359d86298ffc5cf57f0a6e6db41fe2e9ae1cea3f1aea6e8d04059063e9a2e6`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf673715df3431ce0e5b7ecb5a45f804c54f0452668d1739ba0d72eb273b40a`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 20.2 MB (20159366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:6be8d8dc5242f5612f70e4330c87af2c77b03da7b9200bcde42144d7df634672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:8ef8875f2aea79b08c8efa7cd5178a6d9b9593713f40c34cf6ad86e27f799267
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073463613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff54bafe6449abc1b00e591cb11ef385a94d4f4c2a1ef229cd503e0af951d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 14 Dec 2024 01:28:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:58 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:31:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:31:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4bbf7603280e18fef610d62bb0c1efe65eac0d049e0ccbb9c0bb08f368b44`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1294661f7b7b87018d8fb44eb2efa68eec9eb81314c718a493674d32b060b0`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 475.7 KB (475685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d76bd2d48b330e49e4e81c438687e39d7c5fe09bd979da61260f4112a4d7b8`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038de22c9679725e51fb20c3737057ff9ad931bc0725ba5ff42828cd86326f1`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75493ded187a3dc441832ca8c83024487f65272e109da46e3694c0675dc48462`  
		Last Modified: Sat, 14 Dec 2024 01:31:30 GMT  
		Size: 19.0 MB (18998230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9582b154c37509bd6fa7478d4cd602ec5ed1619bd60431de73b99651a2f648`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062405b264d614c41ced78855204ef55a53ddc2103621c8be0f22b4aaff6a0`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d88c5fc0cf0bff6bebbf6f1657990d2898dc69cc5797ebf8e2f656ead725`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833c72764532458c8b7b59609cf6ea55f422a04d6106d24db935ca247026e1f9`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 19.6 MB (19648271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea4c7b5bce6b6df9d1d3810806051f1c595893855de8ce49f45f74ee9341916`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ec6e556fcb04398b6dd8f733bc38bb2bca5be00bfda9edb57e46c3bf8d9410`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf359d86298ffc5cf57f0a6e6db41fe2e9ae1cea3f1aea6e8d04059063e9a2e6`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf673715df3431ce0e5b7ecb5a45f804c54f0452668d1739ba0d72eb273b40a`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 20.2 MB (20159366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c7f73f1e0ebd351f5ae4e99285c52ed240d7af675cbd15a283572e77c4b8d22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:4c61e196683cde572c15fca7d82ec0144d9baf103fc6efb3ae6b0286edd22229
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0c061d2dfcfe6fe2ce770d0b408089cf231775768271407f41c74838440c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 14 Dec 2024 01:28:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:30:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:30:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:30:49 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:30:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf35bbd2931d5fbc55601ef6e88a070c1c0fcc111ab88d99f23348e6cf3a0045`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1808d92f4b99551366b64eae9a9325635d4682408682362e6937d29f5f13db5b`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 357.7 KB (357749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d251f59aac7a5e6567afa4b6afd184f856799c714cda863faddfaf90c90913`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a50f99fd0a08f9d021d34918b3da7a628eb525bcfcfb2a1a1f8c8505f75a37`  
		Last Modified: Sat, 14 Dec 2024 01:31:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310fe7a9d7f781c68c95bb89feff0c0df181313bab50354edffe3ac98fcde4a`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 19.0 MB (18964823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4caff6cb48bd16bcfa5b4883d1b28f4754027b31ec5a130b033f3eb60076018`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d30bfe873c38caa89e51f0346cd5ac3ac398ba811bd23a40b96cb0a371f573`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f185c99ce4f1ffbe43c348be2f1bc873d95393a9c41e5ef71b56efe7d7c39e01`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c0a2d297f342b497a6e32ae77af4ae9310c57d0c28ce7df8100789b50298d2`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 19.6 MB (19615541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e883c865c34857d45a00cf0c21a4565103d0affaf23f50cd7fc717e51e8c5e`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc1a70b9c7b9b3bb4473f12cdf6b227941556b863bea1b52a1a9e7d0d30ebe`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6eaa117645bb79a6c99d1c87cef7a299e6646ea5b44d4252e46259a303c0c8`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2e4fd1f921a57729068da3fb938e48bd7965db83068ceba6e3729c8954d`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 20.1 MB (20133275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4`

```console
$ docker pull docker@sha256:b0c1179ea32ad77bdb7b852b037e54b11022304c2f2662af1954ef53869314b2
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

### `docker:27.4` - linux; amd64

```console
$ docker pull docker@sha256:30564d91cacde37f23816c72f6f86a2d02cbe19d681af326204dce73aee3117a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133445714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8314b971e611487bd98e2907c84df89c10243359ecf1452511dfa5cf594659fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4` - unknown; unknown

```console
$ docker pull docker@sha256:c96c9e5fbcf5f8d775e51157e7dba70c5e097eceb7426fee07d1bd3b0ac3a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058db2570bc3a5e6ac3238878cfc59aa2ecce3aa0b7f01037f9b5744669d9fbc`

```dockerfile
```

-	Layers:
	-	`sha256:bf8e28afb515352bee40ed5d10c10c5be26f8d887c3e7dcdb88dba5cba602f98`  
		Last Modified: Sat, 14 Dec 2024 02:09:01 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4` - linux; arm variant v6

```console
$ docker pull docker@sha256:da6c6379c896b324b06a60ee4a59b170cead5db69a611d58a4a4de4c4c11d306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab07ed540216bdc6189cc7d618da391102c16a16effab1b13dd9bc6eda0f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9b0c55946c0072f1e907f3ee32335a36486a3cd05e42d4e77d30bf8216579f`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 7.0 MB (7037847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d10f548f19c5bba979fcb569834d58e76aff1660a01a0aaf60c9a4a37ca225e`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 89.0 KB (89037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de881962034d29a659cf033f217cf53f013b7f4450e93b99e924b9be583c0d8`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52fc45c7376ba4b93b55bffffddd9b23f5576f74345b1807dbc8f31d852f4a`  
		Last Modified: Sat, 14 Dec 2024 02:08:33 GMT  
		Size: 53.8 MB (53836527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94314352676036e11c60b0e8444d38a745cc65bf67e2c8ed7c05ed9703f28c6b`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16244b8e1e1833788b525bf083eaed44b06a0cd84890a61ac5c17ee22ca6bb27`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4` - unknown; unknown

```console
$ docker pull docker@sha256:a28c353d7c6268dbd78f696ab407329a648ce9b2f7e6d208cc0d81501074fcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c52c05056c0632f86e19f6a07ac6dc323f1f405842cb23a46ebf061095afd28`

```dockerfile
```

-	Layers:
	-	`sha256:10f600e291d01a48cdd062ee030d72c4bf5a329c0e2df55014c65b161f782ccb`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4` - linux; arm variant v7

```console
$ docker pull docker@sha256:7476bf2ec4f13b8681c236b2b26169a5e5a1b3e3067584f5e8f19063f14ab7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122917849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e6717a522d6e5aabe64ab82c5b1fc8b1da3379d43d357f92a6bc13c149f79`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1aaa6f59bd8bea60c22455fb321ddd89ec0b16a6624e1e281e196f100272e`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 6.4 MB (6364981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f179410e55cf07e54cab8edce1e06e30c1dc5cb148acc3674c9c0ecbccc12290`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 85.2 KB (85194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc7ae7d0eef0f8bc25ca2dd6abb99c77404da8155f8f534272a25e7c019722`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b7ae134b8d5df6f3f9c0ad02de62cd38404cbc6c3e675552b0541d3285b1d`  
		Last Modified: Sat, 14 Dec 2024 02:17:21 GMT  
		Size: 53.8 MB (53836568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9884ff30eb5303229cbe20675efa4ca532465af5f9dd1a202dce1db5eeae9410`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9e60dcacfa37d04df6b41f0040e3ff9f4f0a98da2bbee6626e04d41824f0e`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4` - unknown; unknown

```console
$ docker pull docker@sha256:e72cfc40e2a8d6bf2750810862d97a7f8c726a6452405cc30b228325bba2049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e257ba2a900b3722edec07c23b17c8836263c690a781f8754f279c11f3ecea1`

```dockerfile
```

-	Layers:
	-	`sha256:60187e854ca504ec911ae6ac416045a534aec8e7ecf7eb54c3c7d66cf0717f70`  
		Last Modified: Sat, 14 Dec 2024 02:17:18 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:354a62c65fcc5fc052ae7ec2eeee6e556f4fe18fe50eb16e4de9e8e765d6e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125252835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5bf689786a37b6f8dde9e6892fe3e0a3285f204f206b635ab597c8fea8cfa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4` - unknown; unknown

```console
$ docker pull docker@sha256:9b8296cb2db780e6832b39b3e00ee55a8e7797948cd9db9406d948c5cae7a859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0f8db20f775e9edfdb0877cea59a0382cbd87e0ce9ea93717d4088b44fbab`

```dockerfile
```

-	Layers:
	-	`sha256:1c4131432fb5fbd9f96d2130052881001fe65a6a0de6cd98d64efcb94f184edf`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4-cli`

```console
$ docker pull docker@sha256:561338cb111f09a755c9c28e00b66a2466a3dacd88bca6f2f0aeaf909e95730a
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

### `docker:27.4-cli` - linux; amd64

```console
$ docker pull docker@sha256:167c735d631b00384e268f1dd1230ada3bdcac915e749be562481fc37d7cf5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68472707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37409751f89a9183b99563f929bf21325fa6cfcf287679826ec502c1202c3ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:30ad0a07ac64a65ddcd433aeab8a1e559fa50327cb85fa12c22c6b26bdf8763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d0aa13057ebc4ae8e2594681075d7484b2d6e2aa8f0972640a33edf65f20fa`

```dockerfile
```

-	Layers:
	-	`sha256:87259a40baf16e0ae65ac41ce9f8eec992f0fec996d1f945f3c11306b74847e1`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:850519e09ac90396d48c2260b38db241f84f74acb4d372f03ae988d8b1419014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63604936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7f1cecb9a3b1e66edb8ea720a313bd0d7ad69900fee316c2b572c0b2464e12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2d2e4a9727681cfe5637fed05f28442cfeb4e3d4c74b54d1666deea18dbb2f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbfe47a312b92570b77592a48ed008e485b15bb45396495a529a8a455775092`

```dockerfile
```

-	Layers:
	-	`sha256:a14543e98fa59723762ef528b045c1706dfa299cb0a2db5d3c0c940e7ab6e645`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4b6e4baf1ab15df1260382122b976234e24237558bc65513671571609a18bc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0518d1dd421d96cd8f33089a34770da57b68c2740d3b9523f761895f742ed317`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7cdeed720491a6c79999649859d8812011a8a80f99517f4940721f3b106ce4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7cd806863913b1082373e133d60b368631c92a06b92de0243c5876387a0a79`

```dockerfile
```

-	Layers:
	-	`sha256:843f0814593e40fbce871757fbea33ed8b9899f195a215342068a202ad2e0ed3`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a73907930d8ea382a8bfacc5362eb0640cb90f7416b75e42c24bb018694c19dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64440237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71be0f3c62209a33bbb2557f941d3e6e819568152fb39d16dba4e50fa13c6f14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4089d1cdec8b176b873a1d1e877c8bae7d65f093b06b8fbfe1d3e96d0a10cfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e62058998eb61300889bd4e4372fdfce6cc78bde26e2baaa436fcb4b10b0863`

```dockerfile
```

-	Layers:
	-	`sha256:93a1a3e41ef910ab186cf149424caadafef5cf4a7c34e68f789ab980b0483245`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4-dind`

```console
$ docker pull docker@sha256:b0c1179ea32ad77bdb7b852b037e54b11022304c2f2662af1954ef53869314b2
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

### `docker:27.4-dind` - linux; amd64

```console
$ docker pull docker@sha256:30564d91cacde37f23816c72f6f86a2d02cbe19d681af326204dce73aee3117a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133445714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8314b971e611487bd98e2907c84df89c10243359ecf1452511dfa5cf594659fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c96c9e5fbcf5f8d775e51157e7dba70c5e097eceb7426fee07d1bd3b0ac3a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058db2570bc3a5e6ac3238878cfc59aa2ecce3aa0b7f01037f9b5744669d9fbc`

```dockerfile
```

-	Layers:
	-	`sha256:bf8e28afb515352bee40ed5d10c10c5be26f8d887c3e7dcdb88dba5cba602f98`  
		Last Modified: Sat, 14 Dec 2024 02:09:01 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:da6c6379c896b324b06a60ee4a59b170cead5db69a611d58a4a4de4c4c11d306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab07ed540216bdc6189cc7d618da391102c16a16effab1b13dd9bc6eda0f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9b0c55946c0072f1e907f3ee32335a36486a3cd05e42d4e77d30bf8216579f`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 7.0 MB (7037847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d10f548f19c5bba979fcb569834d58e76aff1660a01a0aaf60c9a4a37ca225e`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 89.0 KB (89037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de881962034d29a659cf033f217cf53f013b7f4450e93b99e924b9be583c0d8`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52fc45c7376ba4b93b55bffffddd9b23f5576f74345b1807dbc8f31d852f4a`  
		Last Modified: Sat, 14 Dec 2024 02:08:33 GMT  
		Size: 53.8 MB (53836527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94314352676036e11c60b0e8444d38a745cc65bf67e2c8ed7c05ed9703f28c6b`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16244b8e1e1833788b525bf083eaed44b06a0cd84890a61ac5c17ee22ca6bb27`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a28c353d7c6268dbd78f696ab407329a648ce9b2f7e6d208cc0d81501074fcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c52c05056c0632f86e19f6a07ac6dc323f1f405842cb23a46ebf061095afd28`

```dockerfile
```

-	Layers:
	-	`sha256:10f600e291d01a48cdd062ee030d72c4bf5a329c0e2df55014c65b161f782ccb`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7476bf2ec4f13b8681c236b2b26169a5e5a1b3e3067584f5e8f19063f14ab7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122917849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e6717a522d6e5aabe64ab82c5b1fc8b1da3379d43d357f92a6bc13c149f79`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1aaa6f59bd8bea60c22455fb321ddd89ec0b16a6624e1e281e196f100272e`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 6.4 MB (6364981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f179410e55cf07e54cab8edce1e06e30c1dc5cb148acc3674c9c0ecbccc12290`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 85.2 KB (85194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc7ae7d0eef0f8bc25ca2dd6abb99c77404da8155f8f534272a25e7c019722`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b7ae134b8d5df6f3f9c0ad02de62cd38404cbc6c3e675552b0541d3285b1d`  
		Last Modified: Sat, 14 Dec 2024 02:17:21 GMT  
		Size: 53.8 MB (53836568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9884ff30eb5303229cbe20675efa4ca532465af5f9dd1a202dce1db5eeae9410`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9e60dcacfa37d04df6b41f0040e3ff9f4f0a98da2bbee6626e04d41824f0e`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e72cfc40e2a8d6bf2750810862d97a7f8c726a6452405cc30b228325bba2049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e257ba2a900b3722edec07c23b17c8836263c690a781f8754f279c11f3ecea1`

```dockerfile
```

-	Layers:
	-	`sha256:60187e854ca504ec911ae6ac416045a534aec8e7ecf7eb54c3c7d66cf0717f70`  
		Last Modified: Sat, 14 Dec 2024 02:17:18 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:354a62c65fcc5fc052ae7ec2eeee6e556f4fe18fe50eb16e4de9e8e765d6e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125252835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5bf689786a37b6f8dde9e6892fe3e0a3285f204f206b635ab597c8fea8cfa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9b8296cb2db780e6832b39b3e00ee55a8e7797948cd9db9406d948c5cae7a859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0f8db20f775e9edfdb0877cea59a0382cbd87e0ce9ea93717d4088b44fbab`

```dockerfile
```

-	Layers:
	-	`sha256:1c4131432fb5fbd9f96d2130052881001fe65a6a0de6cd98d64efcb94f184edf`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4-dind-rootless`

```console
$ docker pull docker@sha256:5b6982daa87eac334c19156bfbcaa7931ac5758857d951b05be6136184534394
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.4-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:fc55380e4b93f80c1ed6d12d49cc548099c2cf4fc463a40d2e45a7441a15d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155737519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8322a7c3c8154f09895c7509500e24519267dec8b762f4d2243bd47bfefd97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e959b26a34438101745b4a6b12e2158e837753abb318a703d6a997acee940b32`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 986.6 KB (986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c29d0936b41295dfa648ee92b27ebca2e18c10700ce27472e57dfdbcec4c6a`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d19b2a60bc8d264042588663e4e123d26cbedf4aa96bbcf6ca5483bc82ca2`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50381dd0e19aea2b08429ae4b5824848b0e9e42926ee71822ae02df5e2693d16`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 21.3 MB (21303866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653b8fb52f49b277b1595dfbe1e5b2c3689df958d2df014003ce5cba5b7aa0c7`  
		Last Modified: Sat, 14 Dec 2024 03:07:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f6e358577a60d964b0f1b11ecf89a63cb21351522e15f87d7dfc6ebcda5969ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28cc68cd831df9a34e164fc2ea5b3f364ee6b02cc1f49f036ca59a72bc72571`

```dockerfile
```

-	Layers:
	-	`sha256:644bc1fff97fcf26268d33246cca53014486994146f0e5d4b02de3f5a26c9bcc`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47cd9b46cc39d1ea39ce702f2b197f78006e12d471ac0d9143046b0805d3880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149423499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486e46f1028dafc6440042fcd3a8a6bb5cefda114320b24a99730bc21b9f2484`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1095688739528f200fadd7670e4c7b354566e5b6a5663acc8690e24430f6e3`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.0 MB (1014153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecbf2c620964818ee2dcbc20a175aad27a6fb8b052fb19dd701cbbdb6f23e78`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac17c515dbd19f47019153943183a2995ace4060877f16ef7a715db68ae4181`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8818bf23aa3c08119351a436f05fc62b25a1fa448a59f02e05804a5ab92f00`  
		Last Modified: Sat, 14 Dec 2024 03:07:29 GMT  
		Size: 23.2 MB (23155158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056092e1c446a0219de668b0289797f8369a23417dd278d159af0606bf9b74c5`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f695216a693f4d4041900f72c45a3e39ab19ae5c1727df82414c0e158a605ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c5773897944ec73002da42dd7bafb32c8788aadf785e3ffbd20df78b3d7de2`

```dockerfile
```

-	Layers:
	-	`sha256:732f97201f7324ad6916ceab73e27ea9cf755fc3a41522c77793bdef203efd55`  
		Last Modified: Sat, 14 Dec 2024 03:07:27 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4-windowsservercore`

```console
$ docker pull docker@sha256:533317eb15b02dcd3b6ce9594eb64b19fbb8d5d885addfe2535284535aafcdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27.4-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:4c61e196683cde572c15fca7d82ec0144d9baf103fc6efb3ae6b0286edd22229
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0c061d2dfcfe6fe2ce770d0b408089cf231775768271407f41c74838440c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 14 Dec 2024 01:28:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:30:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:30:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:30:49 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:30:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf35bbd2931d5fbc55601ef6e88a070c1c0fcc111ab88d99f23348e6cf3a0045`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1808d92f4b99551366b64eae9a9325635d4682408682362e6937d29f5f13db5b`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 357.7 KB (357749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d251f59aac7a5e6567afa4b6afd184f856799c714cda863faddfaf90c90913`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a50f99fd0a08f9d021d34918b3da7a628eb525bcfcfb2a1a1f8c8505f75a37`  
		Last Modified: Sat, 14 Dec 2024 01:31:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310fe7a9d7f781c68c95bb89feff0c0df181313bab50354edffe3ac98fcde4a`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 19.0 MB (18964823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4caff6cb48bd16bcfa5b4883d1b28f4754027b31ec5a130b033f3eb60076018`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d30bfe873c38caa89e51f0346cd5ac3ac398ba811bd23a40b96cb0a371f573`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f185c99ce4f1ffbe43c348be2f1bc873d95393a9c41e5ef71b56efe7d7c39e01`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c0a2d297f342b497a6e32ae77af4ae9310c57d0c28ce7df8100789b50298d2`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 19.6 MB (19615541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e883c865c34857d45a00cf0c21a4565103d0affaf23f50cd7fc717e51e8c5e`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc1a70b9c7b9b3bb4473f12cdf6b227941556b863bea1b52a1a9e7d0d30ebe`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6eaa117645bb79a6c99d1c87cef7a299e6646ea5b44d4252e46259a303c0c8`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2e4fd1f921a57729068da3fb938e48bd7965db83068ceba6e3729c8954d`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 20.1 MB (20133275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.4-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:8ef8875f2aea79b08c8efa7cd5178a6d9b9593713f40c34cf6ad86e27f799267
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073463613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff54bafe6449abc1b00e591cb11ef385a94d4f4c2a1ef229cd503e0af951d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 14 Dec 2024 01:28:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:58 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:31:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:31:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4bbf7603280e18fef610d62bb0c1efe65eac0d049e0ccbb9c0bb08f368b44`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1294661f7b7b87018d8fb44eb2efa68eec9eb81314c718a493674d32b060b0`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 475.7 KB (475685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d76bd2d48b330e49e4e81c438687e39d7c5fe09bd979da61260f4112a4d7b8`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038de22c9679725e51fb20c3737057ff9ad931bc0725ba5ff42828cd86326f1`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75493ded187a3dc441832ca8c83024487f65272e109da46e3694c0675dc48462`  
		Last Modified: Sat, 14 Dec 2024 01:31:30 GMT  
		Size: 19.0 MB (18998230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9582b154c37509bd6fa7478d4cd602ec5ed1619bd60431de73b99651a2f648`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062405b264d614c41ced78855204ef55a53ddc2103621c8be0f22b4aaff6a0`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d88c5fc0cf0bff6bebbf6f1657990d2898dc69cc5797ebf8e2f656ead725`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833c72764532458c8b7b59609cf6ea55f422a04d6106d24db935ca247026e1f9`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 19.6 MB (19648271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea4c7b5bce6b6df9d1d3810806051f1c595893855de8ce49f45f74ee9341916`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ec6e556fcb04398b6dd8f733bc38bb2bca5be00bfda9edb57e46c3bf8d9410`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf359d86298ffc5cf57f0a6e6db41fe2e9ae1cea3f1aea6e8d04059063e9a2e6`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf673715df3431ce0e5b7ecb5a45f804c54f0452668d1739ba0d72eb273b40a`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 20.2 MB (20159366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4-windowsservercore-1809`

```console
$ docker pull docker@sha256:6be8d8dc5242f5612f70e4330c87af2c77b03da7b9200bcde42144d7df634672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27.4-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:8ef8875f2aea79b08c8efa7cd5178a6d9b9593713f40c34cf6ad86e27f799267
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073463613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff54bafe6449abc1b00e591cb11ef385a94d4f4c2a1ef229cd503e0af951d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 14 Dec 2024 01:28:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:58 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:31:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:31:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4bbf7603280e18fef610d62bb0c1efe65eac0d049e0ccbb9c0bb08f368b44`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1294661f7b7b87018d8fb44eb2efa68eec9eb81314c718a493674d32b060b0`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 475.7 KB (475685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d76bd2d48b330e49e4e81c438687e39d7c5fe09bd979da61260f4112a4d7b8`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038de22c9679725e51fb20c3737057ff9ad931bc0725ba5ff42828cd86326f1`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75493ded187a3dc441832ca8c83024487f65272e109da46e3694c0675dc48462`  
		Last Modified: Sat, 14 Dec 2024 01:31:30 GMT  
		Size: 19.0 MB (18998230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9582b154c37509bd6fa7478d4cd602ec5ed1619bd60431de73b99651a2f648`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062405b264d614c41ced78855204ef55a53ddc2103621c8be0f22b4aaff6a0`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d88c5fc0cf0bff6bebbf6f1657990d2898dc69cc5797ebf8e2f656ead725`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833c72764532458c8b7b59609cf6ea55f422a04d6106d24db935ca247026e1f9`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 19.6 MB (19648271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea4c7b5bce6b6df9d1d3810806051f1c595893855de8ce49f45f74ee9341916`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ec6e556fcb04398b6dd8f733bc38bb2bca5be00bfda9edb57e46c3bf8d9410`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf359d86298ffc5cf57f0a6e6db41fe2e9ae1cea3f1aea6e8d04059063e9a2e6`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf673715df3431ce0e5b7ecb5a45f804c54f0452668d1739ba0d72eb273b40a`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 20.2 MB (20159366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c7f73f1e0ebd351f5ae4e99285c52ed240d7af675cbd15a283572e77c4b8d22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27.4-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:4c61e196683cde572c15fca7d82ec0144d9baf103fc6efb3ae6b0286edd22229
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0c061d2dfcfe6fe2ce770d0b408089cf231775768271407f41c74838440c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 14 Dec 2024 01:28:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:30:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:30:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:30:49 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:30:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf35bbd2931d5fbc55601ef6e88a070c1c0fcc111ab88d99f23348e6cf3a0045`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1808d92f4b99551366b64eae9a9325635d4682408682362e6937d29f5f13db5b`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 357.7 KB (357749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d251f59aac7a5e6567afa4b6afd184f856799c714cda863faddfaf90c90913`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a50f99fd0a08f9d021d34918b3da7a628eb525bcfcfb2a1a1f8c8505f75a37`  
		Last Modified: Sat, 14 Dec 2024 01:31:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310fe7a9d7f781c68c95bb89feff0c0df181313bab50354edffe3ac98fcde4a`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 19.0 MB (18964823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4caff6cb48bd16bcfa5b4883d1b28f4754027b31ec5a130b033f3eb60076018`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d30bfe873c38caa89e51f0346cd5ac3ac398ba811bd23a40b96cb0a371f573`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f185c99ce4f1ffbe43c348be2f1bc873d95393a9c41e5ef71b56efe7d7c39e01`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c0a2d297f342b497a6e32ae77af4ae9310c57d0c28ce7df8100789b50298d2`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 19.6 MB (19615541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e883c865c34857d45a00cf0c21a4565103d0affaf23f50cd7fc717e51e8c5e`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc1a70b9c7b9b3bb4473f12cdf6b227941556b863bea1b52a1a9e7d0d30ebe`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6eaa117645bb79a6c99d1c87cef7a299e6646ea5b44d4252e46259a303c0c8`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2e4fd1f921a57729068da3fb938e48bd7965db83068ceba6e3729c8954d`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 20.1 MB (20133275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4.1`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-alpine3.21`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-cli`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-cli-alpine3.21`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-dind-alpine3.21`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:cli`

```console
$ docker pull docker@sha256:561338cb111f09a755c9c28e00b66a2466a3dacd88bca6f2f0aeaf909e95730a
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
$ docker pull docker@sha256:167c735d631b00384e268f1dd1230ada3bdcac915e749be562481fc37d7cf5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68472707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37409751f89a9183b99563f929bf21325fa6cfcf287679826ec502c1202c3ae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:30ad0a07ac64a65ddcd433aeab8a1e559fa50327cb85fa12c22c6b26bdf8763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d0aa13057ebc4ae8e2594681075d7484b2d6e2aa8f0972640a33edf65f20fa`

```dockerfile
```

-	Layers:
	-	`sha256:87259a40baf16e0ae65ac41ce9f8eec992f0fec996d1f945f3c11306b74847e1`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:850519e09ac90396d48c2260b38db241f84f74acb4d372f03ae988d8b1419014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63604936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7f1cecb9a3b1e66edb8ea720a313bd0d7ad69900fee316c2b572c0b2464e12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2d2e4a9727681cfe5637fed05f28442cfeb4e3d4c74b54d1666deea18dbb2f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbfe47a312b92570b77592a48ed008e485b15bb45396495a529a8a455775092`

```dockerfile
```

-	Layers:
	-	`sha256:a14543e98fa59723762ef528b045c1706dfa299cb0a2db5d3c0c940e7ab6e645`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4b6e4baf1ab15df1260382122b976234e24237558bc65513671571609a18bc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0518d1dd421d96cd8f33089a34770da57b68c2740d3b9523f761895f742ed317`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:7cdeed720491a6c79999649859d8812011a8a80f99517f4940721f3b106ce4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7cd806863913b1082373e133d60b368631c92a06b92de0243c5876387a0a79`

```dockerfile
```

-	Layers:
	-	`sha256:843f0814593e40fbce871757fbea33ed8b9899f195a215342068a202ad2e0ed3`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a73907930d8ea382a8bfacc5362eb0640cb90f7416b75e42c24bb018694c19dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64440237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71be0f3c62209a33bbb2557f941d3e6e819568152fb39d16dba4e50fa13c6f14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.4.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Fri, 13 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 12:04:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4089d1cdec8b176b873a1d1e877c8bae7d65f093b06b8fbfe1d3e96d0a10cfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e62058998eb61300889bd4e4372fdfce6cc78bde26e2baaa436fcb4b10b0863`

```dockerfile
```

-	Layers:
	-	`sha256:93a1a3e41ef910ab186cf149424caadafef5cf4a7c34e68f789ab980b0483245`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:b0c1179ea32ad77bdb7b852b037e54b11022304c2f2662af1954ef53869314b2
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
$ docker pull docker@sha256:30564d91cacde37f23816c72f6f86a2d02cbe19d681af326204dce73aee3117a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133445714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8314b971e611487bd98e2907c84df89c10243359ecf1452511dfa5cf594659fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:c96c9e5fbcf5f8d775e51157e7dba70c5e097eceb7426fee07d1bd3b0ac3a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058db2570bc3a5e6ac3238878cfc59aa2ecce3aa0b7f01037f9b5744669d9fbc`

```dockerfile
```

-	Layers:
	-	`sha256:bf8e28afb515352bee40ed5d10c10c5be26f8d887c3e7dcdb88dba5cba602f98`  
		Last Modified: Sat, 14 Dec 2024 02:09:01 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:da6c6379c896b324b06a60ee4a59b170cead5db69a611d58a4a4de4c4c11d306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab07ed540216bdc6189cc7d618da391102c16a16effab1b13dd9bc6eda0f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9b0c55946c0072f1e907f3ee32335a36486a3cd05e42d4e77d30bf8216579f`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 7.0 MB (7037847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d10f548f19c5bba979fcb569834d58e76aff1660a01a0aaf60c9a4a37ca225e`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 89.0 KB (89037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de881962034d29a659cf033f217cf53f013b7f4450e93b99e924b9be583c0d8`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52fc45c7376ba4b93b55bffffddd9b23f5576f74345b1807dbc8f31d852f4a`  
		Last Modified: Sat, 14 Dec 2024 02:08:33 GMT  
		Size: 53.8 MB (53836527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94314352676036e11c60b0e8444d38a745cc65bf67e2c8ed7c05ed9703f28c6b`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16244b8e1e1833788b525bf083eaed44b06a0cd84890a61ac5c17ee22ca6bb27`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a28c353d7c6268dbd78f696ab407329a648ce9b2f7e6d208cc0d81501074fcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c52c05056c0632f86e19f6a07ac6dc323f1f405842cb23a46ebf061095afd28`

```dockerfile
```

-	Layers:
	-	`sha256:10f600e291d01a48cdd062ee030d72c4bf5a329c0e2df55014c65b161f782ccb`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7476bf2ec4f13b8681c236b2b26169a5e5a1b3e3067584f5e8f19063f14ab7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122917849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e6717a522d6e5aabe64ab82c5b1fc8b1da3379d43d357f92a6bc13c149f79`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1aaa6f59bd8bea60c22455fb321ddd89ec0b16a6624e1e281e196f100272e`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 6.4 MB (6364981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f179410e55cf07e54cab8edce1e06e30c1dc5cb148acc3674c9c0ecbccc12290`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 85.2 KB (85194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc7ae7d0eef0f8bc25ca2dd6abb99c77404da8155f8f534272a25e7c019722`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b7ae134b8d5df6f3f9c0ad02de62cd38404cbc6c3e675552b0541d3285b1d`  
		Last Modified: Sat, 14 Dec 2024 02:17:21 GMT  
		Size: 53.8 MB (53836568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9884ff30eb5303229cbe20675efa4ca532465af5f9dd1a202dce1db5eeae9410`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9e60dcacfa37d04df6b41f0040e3ff9f4f0a98da2bbee6626e04d41824f0e`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e72cfc40e2a8d6bf2750810862d97a7f8c726a6452405cc30b228325bba2049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e257ba2a900b3722edec07c23b17c8836263c690a781f8754f279c11f3ecea1`

```dockerfile
```

-	Layers:
	-	`sha256:60187e854ca504ec911ae6ac416045a534aec8e7ecf7eb54c3c7d66cf0717f70`  
		Last Modified: Sat, 14 Dec 2024 02:17:18 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:354a62c65fcc5fc052ae7ec2eeee6e556f4fe18fe50eb16e4de9e8e765d6e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125252835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5bf689786a37b6f8dde9e6892fe3e0a3285f204f206b635ab597c8fea8cfa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9b8296cb2db780e6832b39b3e00ee55a8e7797948cd9db9406d948c5cae7a859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0f8db20f775e9edfdb0877cea59a0382cbd87e0ce9ea93717d4088b44fbab`

```dockerfile
```

-	Layers:
	-	`sha256:1c4131432fb5fbd9f96d2130052881001fe65a6a0de6cd98d64efcb94f184edf`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:5b6982daa87eac334c19156bfbcaa7931ac5758857d951b05be6136184534394
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:fc55380e4b93f80c1ed6d12d49cc548099c2cf4fc463a40d2e45a7441a15d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155737519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8322a7c3c8154f09895c7509500e24519267dec8b762f4d2243bd47bfefd97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e959b26a34438101745b4a6b12e2158e837753abb318a703d6a997acee940b32`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 986.6 KB (986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c29d0936b41295dfa648ee92b27ebca2e18c10700ce27472e57dfdbcec4c6a`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d19b2a60bc8d264042588663e4e123d26cbedf4aa96bbcf6ca5483bc82ca2`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50381dd0e19aea2b08429ae4b5824848b0e9e42926ee71822ae02df5e2693d16`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 21.3 MB (21303866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653b8fb52f49b277b1595dfbe1e5b2c3689df958d2df014003ce5cba5b7aa0c7`  
		Last Modified: Sat, 14 Dec 2024 03:07:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f6e358577a60d964b0f1b11ecf89a63cb21351522e15f87d7dfc6ebcda5969ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28cc68cd831df9a34e164fc2ea5b3f364ee6b02cc1f49f036ca59a72bc72571`

```dockerfile
```

-	Layers:
	-	`sha256:644bc1fff97fcf26268d33246cca53014486994146f0e5d4b02de3f5a26c9bcc`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47cd9b46cc39d1ea39ce702f2b197f78006e12d471ac0d9143046b0805d3880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149423499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486e46f1028dafc6440042fcd3a8a6bb5cefda114320b24a99730bc21b9f2484`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1095688739528f200fadd7670e4c7b354566e5b6a5663acc8690e24430f6e3`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.0 MB (1014153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecbf2c620964818ee2dcbc20a175aad27a6fb8b052fb19dd701cbbdb6f23e78`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac17c515dbd19f47019153943183a2995ace4060877f16ef7a715db68ae4181`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8818bf23aa3c08119351a436f05fc62b25a1fa448a59f02e05804a5ab92f00`  
		Last Modified: Sat, 14 Dec 2024 03:07:29 GMT  
		Size: 23.2 MB (23155158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056092e1c446a0219de668b0289797f8369a23417dd278d159af0606bf9b74c5`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f695216a693f4d4041900f72c45a3e39ab19ae5c1727df82414c0e158a605ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c5773897944ec73002da42dd7bafb32c8788aadf785e3ffbd20df78b3d7de2`

```dockerfile
```

-	Layers:
	-	`sha256:732f97201f7324ad6916ceab73e27ea9cf755fc3a41522c77793bdef203efd55`  
		Last Modified: Sat, 14 Dec 2024 03:07:27 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:b0c1179ea32ad77bdb7b852b037e54b11022304c2f2662af1954ef53869314b2
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
$ docker pull docker@sha256:30564d91cacde37f23816c72f6f86a2d02cbe19d681af326204dce73aee3117a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133445714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8314b971e611487bd98e2907c84df89c10243359ecf1452511dfa5cf594659fd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:c96c9e5fbcf5f8d775e51157e7dba70c5e097eceb7426fee07d1bd3b0ac3a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058db2570bc3a5e6ac3238878cfc59aa2ecce3aa0b7f01037f9b5744669d9fbc`

```dockerfile
```

-	Layers:
	-	`sha256:bf8e28afb515352bee40ed5d10c10c5be26f8d887c3e7dcdb88dba5cba602f98`  
		Last Modified: Sat, 14 Dec 2024 02:09:01 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:da6c6379c896b324b06a60ee4a59b170cead5db69a611d58a4a4de4c4c11d306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab07ed540216bdc6189cc7d618da391102c16a16effab1b13dd9bc6eda0f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b2d15f300153712e60e1d5dffec5b74ea2885e4028ca17e58a76e6b1e3f0d`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 16.7 MB (16706367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19653d8a805c6c18e76aa537ab568c5a469036619c05d55f4081997270d244ae`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 17.4 MB (17448131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541d9a6396893504ba5624a0b3eb66cc5a895875061a860c74f42b07f6e647b`  
		Last Modified: Sat, 14 Dec 2024 02:05:16 GMT  
		Size: 18.1 MB (18106561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ffeb8265d69ed0d34fbf2085741244322b730d8d5e622d1454cd238066bf83`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190ecd01efaa323ebcdc0412bdd9a3d381f2f3aeae2d7a403235373ec77a88c`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21f993afde86674e312c4fd365d6d5e0462bb5c676d08196bd12cf44947280`  
		Last Modified: Sat, 14 Dec 2024 02:05:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9b0c55946c0072f1e907f3ee32335a36486a3cd05e42d4e77d30bf8216579f`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 7.0 MB (7037847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d10f548f19c5bba979fcb569834d58e76aff1660a01a0aaf60c9a4a37ca225e`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 89.0 KB (89037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de881962034d29a659cf033f217cf53f013b7f4450e93b99e924b9be583c0d8`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52fc45c7376ba4b93b55bffffddd9b23f5576f74345b1807dbc8f31d852f4a`  
		Last Modified: Sat, 14 Dec 2024 02:08:33 GMT  
		Size: 53.8 MB (53836527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94314352676036e11c60b0e8444d38a745cc65bf67e2c8ed7c05ed9703f28c6b`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16244b8e1e1833788b525bf083eaed44b06a0cd84890a61ac5c17ee22ca6bb27`  
		Last Modified: Sat, 14 Dec 2024 02:08:32 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a28c353d7c6268dbd78f696ab407329a648ce9b2f7e6d208cc0d81501074fcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c52c05056c0632f86e19f6a07ac6dc323f1f405842cb23a46ebf061095afd28`

```dockerfile
```

-	Layers:
	-	`sha256:10f600e291d01a48cdd062ee030d72c4bf5a329c0e2df55014c65b161f782ccb`  
		Last Modified: Sat, 14 Dec 2024 02:08:31 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:7476bf2ec4f13b8681c236b2b26169a5e5a1b3e3067584f5e8f19063f14ab7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122917849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e6717a522d6e5aabe64ab82c5b1fc8b1da3379d43d357f92a6bc13c149f79`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e50a338dc3750f767ab3dd456959998c43867d31b127369e9b5b60a7e50fb5f`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 16.7 MB (16694552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cf4d56d3052052838e9c55d57e875bec151e3a831628d3cabdd0140abffc0`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 17.4 MB (17427590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b534d3f47f9c0021979c390463dce97fd892398c4d8b2fe943c8f3923bf2ab`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 18.1 MB (18092550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3f54b878bfedb15ab245ade3042193246f65c6d198bc650f9efd2e9c5e15`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31218c038bba8024692d489c7f564a2f1cd8cac6b18b862a5d5ef94461c152ed`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0be5cfece2a1c7d657aecbcb9b85d78856f947e9fb51f6c9284bbdaec1228`  
		Last Modified: Sat, 14 Dec 2024 01:30:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1aaa6f59bd8bea60c22455fb321ddd89ec0b16a6624e1e281e196f100272e`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 6.4 MB (6364981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f179410e55cf07e54cab8edce1e06e30c1dc5cb148acc3674c9c0ecbccc12290`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 85.2 KB (85194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc7ae7d0eef0f8bc25ca2dd6abb99c77404da8155f8f534272a25e7c019722`  
		Last Modified: Sat, 14 Dec 2024 02:17:19 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b7ae134b8d5df6f3f9c0ad02de62cd38404cbc6c3e675552b0541d3285b1d`  
		Last Modified: Sat, 14 Dec 2024 02:17:21 GMT  
		Size: 53.8 MB (53836568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9884ff30eb5303229cbe20675efa4ca532465af5f9dd1a202dce1db5eeae9410`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9e60dcacfa37d04df6b41f0040e3ff9f4f0a98da2bbee6626e04d41824f0e`  
		Last Modified: Sat, 14 Dec 2024 02:17:20 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e72cfc40e2a8d6bf2750810862d97a7f8c726a6452405cc30b228325bba2049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e257ba2a900b3722edec07c23b17c8836263c690a781f8754f279c11f3ecea1`

```dockerfile
```

-	Layers:
	-	`sha256:60187e854ca504ec911ae6ac416045a534aec8e7ecf7eb54c3c7d66cf0717f70`  
		Last Modified: Sat, 14 Dec 2024 02:17:18 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:354a62c65fcc5fc052ae7ec2eeee6e556f4fe18fe50eb16e4de9e8e765d6e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125252835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5bf689786a37b6f8dde9e6892fe3e0a3285f204f206b635ab597c8fea8cfa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9b8296cb2db780e6832b39b3e00ee55a8e7797948cd9db9406d948c5cae7a859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b0f8db20f775e9edfdb0877cea59a0382cbd87e0ce9ea93717d4088b44fbab`

```dockerfile
```

-	Layers:
	-	`sha256:1c4131432fb5fbd9f96d2130052881001fe65a6a0de6cd98d64efcb94f184edf`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:533317eb15b02dcd3b6ce9594eb64b19fbb8d5d885addfe2535284535aafcdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:4c61e196683cde572c15fca7d82ec0144d9baf103fc6efb3ae6b0286edd22229
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0c061d2dfcfe6fe2ce770d0b408089cf231775768271407f41c74838440c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 14 Dec 2024 01:28:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:30:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:30:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:30:49 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:30:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf35bbd2931d5fbc55601ef6e88a070c1c0fcc111ab88d99f23348e6cf3a0045`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1808d92f4b99551366b64eae9a9325635d4682408682362e6937d29f5f13db5b`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 357.7 KB (357749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d251f59aac7a5e6567afa4b6afd184f856799c714cda863faddfaf90c90913`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a50f99fd0a08f9d021d34918b3da7a628eb525bcfcfb2a1a1f8c8505f75a37`  
		Last Modified: Sat, 14 Dec 2024 01:31:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310fe7a9d7f781c68c95bb89feff0c0df181313bab50354edffe3ac98fcde4a`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 19.0 MB (18964823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4caff6cb48bd16bcfa5b4883d1b28f4754027b31ec5a130b033f3eb60076018`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d30bfe873c38caa89e51f0346cd5ac3ac398ba811bd23a40b96cb0a371f573`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f185c99ce4f1ffbe43c348be2f1bc873d95393a9c41e5ef71b56efe7d7c39e01`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c0a2d297f342b497a6e32ae77af4ae9310c57d0c28ce7df8100789b50298d2`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 19.6 MB (19615541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e883c865c34857d45a00cf0c21a4565103d0affaf23f50cd7fc717e51e8c5e`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc1a70b9c7b9b3bb4473f12cdf6b227941556b863bea1b52a1a9e7d0d30ebe`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6eaa117645bb79a6c99d1c87cef7a299e6646ea5b44d4252e46259a303c0c8`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2e4fd1f921a57729068da3fb938e48bd7965db83068ceba6e3729c8954d`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 20.1 MB (20133275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:8ef8875f2aea79b08c8efa7cd5178a6d9b9593713f40c34cf6ad86e27f799267
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073463613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff54bafe6449abc1b00e591cb11ef385a94d4f4c2a1ef229cd503e0af951d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 14 Dec 2024 01:28:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:58 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:31:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:31:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4bbf7603280e18fef610d62bb0c1efe65eac0d049e0ccbb9c0bb08f368b44`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1294661f7b7b87018d8fb44eb2efa68eec9eb81314c718a493674d32b060b0`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 475.7 KB (475685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d76bd2d48b330e49e4e81c438687e39d7c5fe09bd979da61260f4112a4d7b8`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038de22c9679725e51fb20c3737057ff9ad931bc0725ba5ff42828cd86326f1`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75493ded187a3dc441832ca8c83024487f65272e109da46e3694c0675dc48462`  
		Last Modified: Sat, 14 Dec 2024 01:31:30 GMT  
		Size: 19.0 MB (18998230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9582b154c37509bd6fa7478d4cd602ec5ed1619bd60431de73b99651a2f648`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062405b264d614c41ced78855204ef55a53ddc2103621c8be0f22b4aaff6a0`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d88c5fc0cf0bff6bebbf6f1657990d2898dc69cc5797ebf8e2f656ead725`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833c72764532458c8b7b59609cf6ea55f422a04d6106d24db935ca247026e1f9`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 19.6 MB (19648271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea4c7b5bce6b6df9d1d3810806051f1c595893855de8ce49f45f74ee9341916`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ec6e556fcb04398b6dd8f733bc38bb2bca5be00bfda9edb57e46c3bf8d9410`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf359d86298ffc5cf57f0a6e6db41fe2e9ae1cea3f1aea6e8d04059063e9a2e6`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf673715df3431ce0e5b7ecb5a45f804c54f0452668d1739ba0d72eb273b40a`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 20.2 MB (20159366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:6be8d8dc5242f5612f70e4330c87af2c77b03da7b9200bcde42144d7df634672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:8ef8875f2aea79b08c8efa7cd5178a6d9b9593713f40c34cf6ad86e27f799267
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073463613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff54bafe6449abc1b00e591cb11ef385a94d4f4c2a1ef229cd503e0af951d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 14 Dec 2024 01:28:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:58 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:31:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:31:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4bbf7603280e18fef610d62bb0c1efe65eac0d049e0ccbb9c0bb08f368b44`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1294661f7b7b87018d8fb44eb2efa68eec9eb81314c718a493674d32b060b0`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 475.7 KB (475685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d76bd2d48b330e49e4e81c438687e39d7c5fe09bd979da61260f4112a4d7b8`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038de22c9679725e51fb20c3737057ff9ad931bc0725ba5ff42828cd86326f1`  
		Last Modified: Sat, 14 Dec 2024 01:31:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75493ded187a3dc441832ca8c83024487f65272e109da46e3694c0675dc48462`  
		Last Modified: Sat, 14 Dec 2024 01:31:30 GMT  
		Size: 19.0 MB (18998230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9582b154c37509bd6fa7478d4cd602ec5ed1619bd60431de73b99651a2f648`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062405b264d614c41ced78855204ef55a53ddc2103621c8be0f22b4aaff6a0`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d88c5fc0cf0bff6bebbf6f1657990d2898dc69cc5797ebf8e2f656ead725`  
		Last Modified: Sat, 14 Dec 2024 01:31:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833c72764532458c8b7b59609cf6ea55f422a04d6106d24db935ca247026e1f9`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 19.6 MB (19648271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea4c7b5bce6b6df9d1d3810806051f1c595893855de8ce49f45f74ee9341916`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ec6e556fcb04398b6dd8f733bc38bb2bca5be00bfda9edb57e46c3bf8d9410`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf359d86298ffc5cf57f0a6e6db41fe2e9ae1cea3f1aea6e8d04059063e9a2e6`  
		Last Modified: Sat, 14 Dec 2024 01:31:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf673715df3431ce0e5b7ecb5a45f804c54f0452668d1739ba0d72eb273b40a`  
		Last Modified: Sat, 14 Dec 2024 01:31:29 GMT  
		Size: 20.2 MB (20159366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c7f73f1e0ebd351f5ae4e99285c52ed240d7af675cbd15a283572e77c4b8d22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:4c61e196683cde572c15fca7d82ec0144d9baf103fc6efb3ae6b0286edd22229
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0c061d2dfcfe6fe2ce770d0b408089cf231775768271407f41c74838440c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 14 Dec 2024 01:28:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 01:30:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_VERSION=27.4.0
# Sat, 14 Dec 2024 01:30:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Sat, 14 Dec 2024 01:30:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:36 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Sat, 14 Dec 2024 01:30:37 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Sat, 14 Dec 2024 01:30:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 14 Dec 2024 01:30:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Sat, 14 Dec 2024 01:30:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-windows-x86_64.exe
# Sat, 14 Dec 2024 01:30:49 GMT
ENV DOCKER_COMPOSE_SHA256=b18f79e01e22362faede43844a2131038c49b52692150deb8ea81f98ab286fe6
# Sat, 14 Dec 2024 01:30:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf35bbd2931d5fbc55601ef6e88a070c1c0fcc111ab88d99f23348e6cf3a0045`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1808d92f4b99551366b64eae9a9325635d4682408682362e6937d29f5f13db5b`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 357.7 KB (357749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d251f59aac7a5e6567afa4b6afd184f856799c714cda863faddfaf90c90913`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a50f99fd0a08f9d021d34918b3da7a628eb525bcfcfb2a1a1f8c8505f75a37`  
		Last Modified: Sat, 14 Dec 2024 01:31:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310fe7a9d7f781c68c95bb89feff0c0df181313bab50354edffe3ac98fcde4a`  
		Last Modified: Sat, 14 Dec 2024 01:31:03 GMT  
		Size: 19.0 MB (18964823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4caff6cb48bd16bcfa5b4883d1b28f4754027b31ec5a130b033f3eb60076018`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d30bfe873c38caa89e51f0346cd5ac3ac398ba811bd23a40b96cb0a371f573`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f185c99ce4f1ffbe43c348be2f1bc873d95393a9c41e5ef71b56efe7d7c39e01`  
		Last Modified: Sat, 14 Dec 2024 01:31:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c0a2d297f342b497a6e32ae77af4ae9310c57d0c28ce7df8100789b50298d2`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 19.6 MB (19615541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e883c865c34857d45a00cf0c21a4565103d0affaf23f50cd7fc717e51e8c5e`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc1a70b9c7b9b3bb4473f12cdf6b227941556b863bea1b52a1a9e7d0d30ebe`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6eaa117645bb79a6c99d1c87cef7a299e6646ea5b44d4252e46259a303c0c8`  
		Last Modified: Sat, 14 Dec 2024 01:30:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2e4fd1f921a57729068da3fb938e48bd7965db83068ceba6e3729c8954d`  
		Last Modified: Sat, 14 Dec 2024 01:31:02 GMT  
		Size: 20.1 MB (20133275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
