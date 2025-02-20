## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:4fd33b542fd19c2416a18be3d260a2168042b87829f9c3dc31a75acc8d2fb9e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:065213279880e2930e2a55feb4fbce16a7b8e3d5b360c7259364d6b6ddcdc1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157518234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d434f53db6965c4612de42a9a2f09c2cb884baccd5d0fb372b351e4b9a62f61`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_VERSION=28.0.0-rc.3
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Feb 2025 00:04:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD ["sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Feb 2025 00:04:40 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD []
# Wed, 19 Feb 2025 00:04:40 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 19 Feb 2025 00:04:40 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aaf86294e20a08869e62f102687e1a19149fab47342f7bbae209ae4723dc569`  
		Last Modified: Wed, 19 Feb 2025 19:27:34 GMT  
		Size: 8.1 MB (8062969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e912116c79aff248a322e4ff551a41ab56412dbb6b6d4026d41782521a9f8a`  
		Last Modified: Wed, 19 Feb 2025 19:27:32 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515ddf0af814829b15136e59a16be2d0eb62e7292ef3c35d9b37b04fd003a41d`  
		Last Modified: Wed, 19 Feb 2025 19:27:38 GMT  
		Size: 19.5 MB (19492203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420764532edc8d5531861800eb911c8c050756c37bca7a6b43481d9354ca30a0`  
		Last Modified: Wed, 19 Feb 2025 19:27:37 GMT  
		Size: 20.2 MB (20234558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9ad968c592bdaf775a13b18d8c158bd629437a6b295bf467b20fce0edf4106`  
		Last Modified: Wed, 19 Feb 2025 19:27:37 GMT  
		Size: 20.9 MB (20907752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085d56e5e5b1e345928d1affd42c476dc0da83272f84c6579fc96827e618a0c3`  
		Last Modified: Wed, 19 Feb 2025 19:27:34 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b451a705f54bd9322b0af4aa948f7b8687b6ed7eec476fc962f45a137c75ba4c`  
		Last Modified: Wed, 19 Feb 2025 19:27:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5016cfbd98dfb93b621c700514b0fe7f94e896ad92879362eaff8e0e745aac20`  
		Last Modified: Wed, 19 Feb 2025 19:27:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfaf9e09c8841fc8914e7b30230a16792aaff0656a440e7870d93f9a102d4a4`  
		Last Modified: Wed, 19 Feb 2025 20:28:59 GMT  
		Size: 6.7 MB (6733047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e38ce42a0c13c027e61f13b788bcd4deda12d584244eca48e4a474aa2004c`  
		Last Modified: Wed, 19 Feb 2025 20:28:51 GMT  
		Size: 90.3 KB (90320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192132175ab3c70eec860a50665c32a2546e4e99719a004c108b7d09e91126b2`  
		Last Modified: Wed, 19 Feb 2025 20:28:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49fb1a9d02172a2c473bfec29d81f6486fb45b12bb77cfd07c46fb9b4652f10`  
		Last Modified: Wed, 19 Feb 2025 20:29:08 GMT  
		Size: 60.2 MB (60192772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b4fbe34aeae0f0e24c508fe58b067a4f83665a5c7d9dcd3383b2e7a7df829c`  
		Last Modified: Wed, 19 Feb 2025 20:28:49 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473c6b786ad27d86a1865b1cc723edbcebc828fad29041271757dc2453d4b63e`  
		Last Modified: Wed, 19 Feb 2025 20:28:49 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f847804cb427141e237235436d500e3d866d149c40fbae4cf14242e6b515869c`  
		Last Modified: Wed, 19 Feb 2025 21:29:31 GMT  
		Size: 986.6 KB (986574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae039d7bdd7a50c178f8fecac18170fb7ca8ba4cb7196bffe29f0980096fe43c`  
		Last Modified: Wed, 19 Feb 2025 21:29:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61759e19290bd127ff067d36d83c1af807caade744df6554378b8fd9cbfaa4e4`  
		Last Modified: Wed, 19 Feb 2025 21:29:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4949242e58cf3fcce4f3f7e8c1e4e634908ecb2231a8e6276b14f6609dae51b6`  
		Last Modified: Wed, 19 Feb 2025 21:29:39 GMT  
		Size: 17.2 MB (17166397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624b0695e77d74bb0c47abae24256bc18bf683b580723b81d424fa126e83597f`  
		Last Modified: Wed, 19 Feb 2025 21:29:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1714b0837c8b3014be6563b66216f0bf9dd94f46d534af535400ee9305609005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a19a0c050d1965ff48793e0d4c7aff4ae321efb80e2a0b0ade85dba6fdcd72`

```dockerfile
```

-	Layers:
	-	`sha256:5f864043b93b3f75ae2779bfefe862f38f191d7f719dbfb685be7fd78211ce36`  
		Last Modified: Thu, 20 Feb 2025 00:08:16 GMT  
		Size: 30.2 KB (30203 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:85cc78a0d895d0d9a8f7e91299d6df338689d08c764d504975e847e3bbe9f05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151062362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b56e2ee36c64316f10a15940e4c0cb73c70a22ea035022109e83e2e50c39a9a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_VERSION=28.0.0-rc.3
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Feb 2025 00:04:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD ["sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Feb 2025 00:04:40 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD []
# Wed, 19 Feb 2025 00:04:40 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 19 Feb 2025 00:04:40 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ac8b8412c3ffa81dcde5740aef1953c47f791be525bcb421e89bc9051e6bad`  
		Last Modified: Wed, 19 Feb 2025 19:26:14 GMT  
		Size: 8.1 MB (8076372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c517bd3bb254433972817513e72788f2394e42d64f5e7de914be9b4990fec21d`  
		Last Modified: Wed, 19 Feb 2025 19:26:13 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d9d462aa77ec007fbeffc1dee42df4cd4a71183e9e8428cdd7953d37bf652`  
		Last Modified: Wed, 19 Feb 2025 19:26:15 GMT  
		Size: 18.4 MB (18413407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ebefb617d29bf3d664c14a93a8d6af6169ff30bede662b6427222e19ead23e`  
		Last Modified: Wed, 19 Feb 2025 19:26:16 GMT  
		Size: 18.5 MB (18457784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfde26c05a0c43440279088e13663a7a1d54d60fc79a334f7efc7c2d97ac5cf4`  
		Last Modified: Wed, 19 Feb 2025 19:26:15 GMT  
		Size: 19.2 MB (19175087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63356e70e776cf3f69c9c71c36110eef0d389fa3d3031f61530a5690b4aef020`  
		Last Modified: Wed, 19 Feb 2025 19:26:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623035a000b7c0fd3795aadbe0a1896ab131817b4d53c047c6698f65f4c910ab`  
		Last Modified: Wed, 19 Feb 2025 19:26:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c85bbe716c49f7bb8731d7ac0bf65f0b6d6d65a93e1d5f9344d3cca378f284`  
		Last Modified: Wed, 19 Feb 2025 19:26:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77018210f192a8f3a153def365573764b3b2bbc2a225a7d7f121de0d359ba4`  
		Last Modified: Wed, 19 Feb 2025 20:33:00 GMT  
		Size: 7.0 MB (6978851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46306e777430bd461589041ef5e1b2732743f437985659be3ff93ced09d8042`  
		Last Modified: Wed, 19 Feb 2025 20:32:51 GMT  
		Size: 99.4 KB (99381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0afecbb84ea048248cd26c2553798898a1f1856a9c2318f81b40e47798954`  
		Last Modified: Wed, 19 Feb 2025 20:32:50 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ef1d8041a787834ea307ebc08a6c7a732c521fad26992f0fe82409b302de6a`  
		Last Modified: Wed, 19 Feb 2025 20:33:07 GMT  
		Size: 55.6 MB (55565415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b553d4ac0e9d181c727f58d22104b70b1db592d987dd2d81dbe68c047bef9`  
		Last Modified: Wed, 19 Feb 2025 20:32:50 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ec7eb8ba81e2cf67cea95fbf7089386677fae3ccd50d30918e4dfda64151b6`  
		Last Modified: Wed, 19 Feb 2025 20:32:49 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482ed1cdcef81bebd3affda29641f827c2654395c8ac2348e5beab3727dbd1a1`  
		Last Modified: Wed, 19 Feb 2025 21:32:53 GMT  
		Size: 1.0 MB (1014201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa4132894075ceed58ad1afcfb145b3fe824ae6d32198d1a9e1155fe17548bf`  
		Last Modified: Wed, 19 Feb 2025 21:32:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f83038f687b0e3ce29120992050d7be0c7454ebac6a3a92386e6f32fb8e49a`  
		Last Modified: Wed, 19 Feb 2025 21:32:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abd75686941fbaf99c44bac9b929cfdba086557b1d8fb0ca6d81714e8f2db90`  
		Last Modified: Wed, 19 Feb 2025 21:33:02 GMT  
		Size: 19.3 MB (19279427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6cb37a9e5941afd5b0435bd1443360507bff1c6e2b2d3791628b518a6e848a`  
		Last Modified: Wed, 19 Feb 2025 21:32:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:599d7659d0b8a5caf497e8dbca8ad4dd5b448b3a24bb2214a1f50d657569d5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dff962928951f0d604e0675f09b9f166ea05ac4ab236a2cce39936f34d263f7`

```dockerfile
```

-	Layers:
	-	`sha256:0281a16f591630add279b0756bac274bfededfe5da8c4546c5476bdf311ce49a`  
		Last Modified: Thu, 20 Feb 2025 00:08:17 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json
