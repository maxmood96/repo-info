## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:428f67d86d6bc47c6f0cc709daec77cab4817c4863682505660f72855d838742
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:43fe0cd2a2248857864fcb20d0fc5aeb40fefa472fd39623e7d6ce1a50a8135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157340651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327f0b66cc738ae16439837b198b58e5bcc36020f967ec2fca849633201e9f2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_VERSION=27.4.0-rc.2
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64'; 			sha256='fbb4853d3f2148b0f2f0916f8971c9e500784e4e4949324934fc0b7dc2ed5016'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv6'; 			sha256='7116c73bd22504ff61e5e25f3ea6638a7b2a5d126764fccdec4fd7623cf17963'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv7'; 			sha256='944402b85b5eb8492ebbe2e4dcbf962adcaaa16b0ed66b51abaf2ac3e3809b1b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-aarch64'; 			sha256='8fed7b79b8bd1cb0624142f7d723c3cc67ba747c77ed69abbdefdc77a6d416d1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-ppc64le'; 			sha256='9a5d9fd85e852a9c3c9137ea8ea80d66f0fe349d34b3e329255d98cd960c331e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-riscv64'; 			sha256='eda617db72d24fe79be98e2273e1fb433943a18479cedc86601963f75666304f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-s390x'; 			sha256='9476a64e9605df956e3e33b09acfdaed2d4a2c71da5b4a09899a9b7d428263a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Nov 2024 18:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
CMD ["sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Nov 2024 18:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 Nov 2024 18:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
CMD []
# Tue, 19 Nov 2024 18:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Nov 2024 18:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6131ee63a03c7076ea9f96c235a1a828736b73d1f9f51430f1322d5f1cc6d4a`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 7.9 MB (7889960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b99a75f75a4a873cdf98bd1d4ef617bfbc27c29628a5ab321ac5c2a24387d`  
		Last Modified: Wed, 20 Nov 2024 00:24:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b6df9a88c151a5dc4ba38fcb0390a6207409742522be361393a4f19a62c6a5`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 18.7 MB (18669680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da018fe6e4d31a39253a3cf8c83686783423d438a3cd860f15b064fbb41382c3`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 18.6 MB (18566631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e47c26206dbe9c1266e0627a21066cabc6bb631edb1ff9153c62f72dd6b4e6`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 19.1 MB (19117165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ef5d990fb9edb79d69620ce3b9f18fab9cec40f504d58e75705d5d8f6182f1`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70b870fecb7e8167d660ef5b43e093090fc0465e0e91987b32323165111f115`  
		Last Modified: Wed, 20 Nov 2024 00:24:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fbc59c10f6357948def92e7254adb472d0ea8810599b1cd4f434a5968eb7c4`  
		Last Modified: Wed, 20 Nov 2024 00:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003828f788e7884141757b30a038b71614e402ef452e28c3ac98ec5ccbcf95b`  
		Last Modified: Wed, 20 Nov 2024 01:07:39 GMT  
		Size: 9.1 MB (9067188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbae3e5a2db4737b866bb32255b1c37a02d99490d806590471cd28089d42528`  
		Last Modified: Wed, 20 Nov 2024 01:07:39 GMT  
		Size: 89.2 KB (89235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dff9f40e2632b19855e69cdf10ed7cfc564c499108c73859009093c6ff3ec2e`  
		Last Modified: Wed, 20 Nov 2024 01:07:39 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c532dad38c982166b2551b57fae679489dd7005a39763c0e7be04c960b0f35b`  
		Last Modified: Wed, 20 Nov 2024 01:07:40 GMT  
		Size: 58.0 MB (58022762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ce1a444fa5dd102b39f60d65743aef39142590de6f2599f89ee30d4c8830f2`  
		Last Modified: Wed, 20 Nov 2024 01:07:40 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de1bcb30072177dd84f05769e8e258bdbb0288d7c389379f30ce00d96fc64e7`  
		Last Modified: Wed, 20 Nov 2024 01:07:40 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00a51c1f634f4c9f947e3f3abeea3410a10912c034d248aacca0c5a9addb39`  
		Last Modified: Wed, 20 Nov 2024 02:11:09 GMT  
		Size: 981.6 KB (981581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be23c86c967c4f004cf94e293009ca372ba2acf84d037f2c38f6ab7f09179fa`  
		Last Modified: Wed, 20 Nov 2024 02:11:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b3c34e2cdeb00a6ec40fe83ca1674cf02ff793c4fd5d7d144311238ea1012`  
		Last Modified: Wed, 20 Nov 2024 02:11:09 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3e06b06212b0f5f13a47e1979dba1b5390dcd73d1d953975cde83b801a73e8`  
		Last Modified: Wed, 20 Nov 2024 02:11:09 GMT  
		Size: 21.3 MB (21303253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd6f8338967ce18eccd435e6e0d41838182d45d3df9a2ce0b2bc06fee45cbb7`  
		Last Modified: Wed, 20 Nov 2024 02:11:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:670a6146fb7222a129ffe1116f52f79c393987cec840182b2a92b358436e42d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e1211663c9e0644bd66c575609f8e84568dca166288006654116098bb5b71b`

```dockerfile
```

-	Layers:
	-	`sha256:dde74f29a060434a7bc3f4cd6aaa193cae1d55ef146b9b78e85788e88a67830f`  
		Last Modified: Wed, 20 Nov 2024 02:11:09 GMT  
		Size: 30.4 KB (30369 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4e707f345ee1ee121db45d139bda698101dbc0fa8d88885a36037d5bae0d4d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151866576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e99cc8f8669c7de9d291a3321fd97410d71a0a193aeed8a512c8f10f00ca46`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_VERSION=27.4.0-rc.2
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64'; 			sha256='fbb4853d3f2148b0f2f0916f8971c9e500784e4e4949324934fc0b7dc2ed5016'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv6'; 			sha256='7116c73bd22504ff61e5e25f3ea6638a7b2a5d126764fccdec4fd7623cf17963'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv7'; 			sha256='944402b85b5eb8492ebbe2e4dcbf962adcaaa16b0ed66b51abaf2ac3e3809b1b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-aarch64'; 			sha256='8fed7b79b8bd1cb0624142f7d723c3cc67ba747c77ed69abbdefdc77a6d416d1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-ppc64le'; 			sha256='9a5d9fd85e852a9c3c9137ea8ea80d66f0fe349d34b3e329255d98cd960c331e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-riscv64'; 			sha256='eda617db72d24fe79be98e2273e1fb433943a18479cedc86601963f75666304f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-s390x'; 			sha256='9476a64e9605df956e3e33b09acfdaed2d4a2c71da5b4a09899a9b7d428263a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Nov 2024 18:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
CMD ["sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Nov 2024 18:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 Nov 2024 18:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
CMD []
# Tue, 19 Nov 2024 18:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Nov 2024 18:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c2943fcc4c049fb6a537793b27e1f49f7fbf03dccba1f916dffc11bf201c22`  
		Last Modified: Wed, 20 Nov 2024 00:24:42 GMT  
		Size: 8.0 MB (7998165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb19f166db867e8841734ae49cc6de3ff5e775f528caefeca64e45c74d72a75`  
		Last Modified: Wed, 20 Nov 2024 00:24:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7399e06c10a10d4b2338d3e8f5a1d38337678a02b582214d7cce00efde54c83`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 17.6 MB (17619942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a2fdee375f19d800d1c3b9f7eb17d6333c9e65fedf1839b41f0b736282d9fd`  
		Last Modified: Wed, 20 Nov 2024 00:24:42 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa5086a97056f2dd54bf2822cbb50efeb702abe4c58e6cc7b2bbea7084d2b4e`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 17.5 MB (17489942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63283e47922e1addd6aefeb0a95800495d23942e877fec9bd8c3b0cbc072a6de`  
		Last Modified: Wed, 20 Nov 2024 00:24:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8439390d1e56e7c03233d875d55345d5b0a70be6a0423c5d923cc02ac86dc7`  
		Last Modified: Wed, 20 Nov 2024 00:24:44 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdf0388e567e31b4ae89d097b0d536a143ef34bcadd4804ff36d7940849e286`  
		Last Modified: Wed, 20 Nov 2024 00:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1947b4c47fb16179408481f4eb141f1e24c412f05704adb0ce8fe12c69a85b28`  
		Last Modified: Wed, 20 Nov 2024 01:07:26 GMT  
		Size: 9.9 MB (9854532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccbd1e5df7e13468530d95f6a2037740bfdc85421620aee47b70f9e6f49f3c7`  
		Last Modified: Wed, 20 Nov 2024 01:07:26 GMT  
		Size: 98.7 KB (98660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49fd2d46af5d4b6baaeeb50693a9e720ace3763f4f879abab41e826b1f2108a`  
		Last Modified: Wed, 20 Nov 2024 01:07:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d56ff2075a0e0f65dc9196b76485511d627bdc80fe6b9788b3780cd89895789`  
		Last Modified: Wed, 20 Nov 2024 01:07:27 GMT  
		Size: 53.6 MB (53623757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd38104c887c5ca084596f9434e6ea5eecc44566ac9b99bbbc9b3ffd1d68ae8`  
		Last Modified: Wed, 20 Nov 2024 01:07:26 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1774b93662bd3705c185b3859d59d836046419f3c63c035346f9d5323d0db5e`  
		Last Modified: Wed, 20 Nov 2024 01:07:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57c0c1f17806e05dc826939abe479e0a49215c5bd114f5f3f1263d5e5db5be`  
		Last Modified: Wed, 20 Nov 2024 02:07:26 GMT  
		Size: 1.0 MB (1023832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8f7b7512fe668da279f450a1fbc3bfa7152869850f79e82f7ab5e37da81223`  
		Last Modified: Wed, 20 Nov 2024 02:07:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe4d3f949cb427b4b1c2e57da68eb3f7190a0d14cb535a745e3439816249af7`  
		Last Modified: Wed, 20 Nov 2024 02:07:25 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36e404f6851976c8ecc58c5419cb6d277ba16128d31e751eba47faa9a3208e`  
		Last Modified: Wed, 20 Nov 2024 02:07:27 GMT  
		Size: 23.2 MB (23155543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08452e49379ff4821308a12bbd57db262fda64bdc86dd9138424fc28452c005e`  
		Last Modified: Wed, 20 Nov 2024 02:07:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b4b920fea6c15c5e5a8094778376f1be3004d69a8ccc42eddd8bcee34eef155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba1e1825ffe9f950747487ef0d48af747bc2491a282bea23b30a79204355f9c`

```dockerfile
```

-	Layers:
	-	`sha256:c6a53381b16d3917ee9ca7dc394c638d0fd7f56d135a3988d3e4e48d911435d6`  
		Last Modified: Wed, 20 Nov 2024 02:07:25 GMT  
		Size: 30.5 KB (30526 bytes)  
		MIME: application/vnd.in-toto+json
