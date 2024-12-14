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
