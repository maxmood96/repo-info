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
