## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:7779bdf6410d7018314dc01fa7b5d1bc454f79043e7e79cd8d2280c0eb175d5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ad1978a4beba02584cc95f4bcda85fc558626574fa7e3a31d7e347c51fb6a3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154125879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab771474a4cc2240f185cc3dabe6f854247020033a35c115ca4684b0e2655ab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6c7a74a9684496321c016d9b66ea0bd25b6ec495850a4cf0776ee8d998716e`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 7.9 MB (7872619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9083bbbcc63434adc2e7efdfbff5ac4f433f94d3038a6e3e8659121b9e293d`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e26ebe780c9dd11d906302408170ba7c7ed6769701bac928683240791e141d5`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 18.6 MB (18601178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c91be66a8062aea42b5620a48831317a9f22e77823afd9286926fc69937443`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 18.4 MB (18404797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb04b7eee4536f48184c875f07f490c58813d5322b94e84da5f0088cba37a4b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 18.8 MB (18825282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decc4c3a5d181ee1a3037e299cc54939eaa5b7568fa52d403e16dd6a9217cc09`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759be82af79cabcd02f5cb42aae48bb2596900392cd1ed0d177ca43ec1eddfbd`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0252e41ddc3d0b47674578bb5e3aaca69b3891b9d9ef3a2b900a5fb8946f21`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb86ffeb96f2d03f6e66a55c87d3b9bb02f4c4247d1a74abc7fe25cd5c2bd8d`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 6.7 MB (6657982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16f59cbb64274ca5d52640b25b822fa545f3411272612de56a0c132e19e3e2e`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e5a29d28a128a6a806ae2bd361c0c5b8267735e49ff1d4d915913ceb9a5421`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf967b7f653e403afab003a31c2f7c874aae8feaba04cf77d1cef057326bef1`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 57.8 MB (57773387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6aa706598304880925550b1ba9ecba5c5b561644312944ba393f6be933f4f7`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2818ec033535f4f06aa3fa211c70f85bfa81dd7a5da263414b9045c5d3dc0a47`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b0ed7b7a8982badb7baced9e52d8783c10251cd4bc05f6f264d5e93fccfd0`  
		Last Modified: Tue, 10 Sep 2024 01:01:32 GMT  
		Size: 981.0 KB (980984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269025022fb53c47af86ef9483f30b1dfc8b9c72381b9c4fc336259a4b7f05e4`  
		Last Modified: Tue, 10 Sep 2024 01:01:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4947889ef63d881179381cb4447baa60e66b866e4699f94cc8d44e5ca51d0b`  
		Last Modified: Tue, 10 Sep 2024 01:01:31 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d078ea32dcd6ea19a5aee8eaed858f3e35b909e852ce8d078b3662ba221fc6e`  
		Last Modified: Tue, 10 Sep 2024 01:01:32 GMT  
		Size: 21.3 MB (21287322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79a9a639441d2f13441d658f487fe8322263109de0ab4ccfbf08208ec027ba`  
		Last Modified: Tue, 10 Sep 2024 01:01:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2f5d9a31bdf3f852985a8866e4be2160dde449c137eae034edc004e314a8c161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e55b08059bf1a08614498bae2b0f353464a429591761c5700f63aeef16eb3e`

```dockerfile
```

-	Layers:
	-	`sha256:4e879fbd77d397aca961c4bc156532408c72ed9044977530f24acef2fbc8672d`  
		Last Modified: Tue, 10 Sep 2024 01:01:31 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c6b25abd92845edffc876ad45dd8b8b8c65c87c62e1e6e1770767a62bc728d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146697453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c730af298cecc77a70711071ddac64045d33a481536b49d7e0827765d56f65`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 27 Aug 2024 23:04:15 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.2.0
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 27 Aug 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
CMD ["sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
VOLUME [/var/lib/docker]
# Tue, 27 Aug 2024 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 27 Aug 2024 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
CMD []
# Tue, 27 Aug 2024 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Aug 2024 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460264657750f777bab3101369ff9aafc3c0f9a31e1cff8bd4a8a56b1da19b74`  
		Last Modified: Sat, 07 Sep 2024 04:49:06 GMT  
		Size: 8.0 MB (7981907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234fc0fe38a86ca70e84b7d7ff4bf018108637751c7ef3e65fbb786e8ba8015e`  
		Last Modified: Sat, 07 Sep 2024 04:49:05 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ef915ef5d4921b502359c5384d94b6ef9098724278cfbf0432b1176db5f1cf`  
		Last Modified: Sat, 07 Sep 2024 04:49:06 GMT  
		Size: 17.3 MB (17266026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0271230737793b4604f5fae5edba0cca809ef52ffd6cfcedc9c972c7afb360d`  
		Last Modified: Sat, 07 Sep 2024 04:49:06 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2509d5aa2e240e727a095dc90b5e5e543d1e39f2fcdba08821e5faeb10bd174`  
		Last Modified: Sat, 07 Sep 2024 04:49:07 GMT  
		Size: 17.2 MB (17186840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437adbd2fd1035b667fe5c2dd1bb68663f00a39911412bec314e55482064708`  
		Last Modified: Sat, 07 Sep 2024 04:49:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fce3123f6ec5b360de3d2d8769246a1880ed2d813b89a3a6c881d35cf23dd3`  
		Last Modified: Sat, 07 Sep 2024 04:49:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdc11613b2be74236c0b83f77d4f069d85331774ca54599dfd8811f4017f75b`  
		Last Modified: Sat, 07 Sep 2024 04:49:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21c75d73018024a1bd2dfb9fe5268e12d79355a390aab089e790de7444a7e03`  
		Last Modified: Sat, 07 Sep 2024 12:27:46 GMT  
		Size: 7.0 MB (7034852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aafc606bf8d72a10d8e8dc00cf359c00b1dfa52dbb3780fddd8c457a5c21a4`  
		Last Modified: Sat, 07 Sep 2024 12:27:46 GMT  
		Size: 98.6 KB (98646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaafcd0d7c3270d7ee64b626998e3cf594236d46ee223fb54b09396f1686c7e`  
		Last Modified: Sat, 07 Sep 2024 12:27:46 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06841fb84d32dcb28de41ef5b3d0eb8429737f9f1439ccf54ae75ae171c194`  
		Last Modified: Sat, 07 Sep 2024 12:27:47 GMT  
		Size: 52.4 MB (52400281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aee60cb8c24d37aea6782b2aa08a69368dd0b3af5ad6bf5b94b59de76e1613c`  
		Last Modified: Sat, 07 Sep 2024 12:27:47 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886ec2268d68c7b9c962d06fde10cb1de5eed49ea4a2e7682ec1b2d63b44901e`  
		Last Modified: Sat, 07 Sep 2024 12:27:46 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a792957b8aeabecfd903a0764c9a1f21ab182dcc8e11074ec8b69c39e39b421f`  
		Last Modified: Sat, 07 Sep 2024 14:07:52 GMT  
		Size: 1.0 MB (1023125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1f706fb243c83335093c8876b97046f145c2078a1b55f45b728b62a0bc03d4`  
		Last Modified: Sat, 07 Sep 2024 14:07:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a39c616762bc2f3658a9daa0658ebbb50cd8916a9e039d6fb7a2c3f5d0e4a3`  
		Last Modified: Sat, 07 Sep 2024 14:07:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85acd0437c9172d2aad7a900aeca0bc961e53d1c67e3342055239ce468c43942`  
		Last Modified: Sat, 07 Sep 2024 14:07:53 GMT  
		Size: 22.8 MB (22835867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b73ab8f21bc1b191bbc918da5c820773c246fb79f98e0ab57b232ca8e418130`  
		Last Modified: Sat, 07 Sep 2024 14:07:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a4f84bc6868f736d63dd82b4992dda752b5e47b28fcdfa005e71ba40bbf5fd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23e533bc0007ac9fd67fc88acc844af86897e3fb58011b537c063334405fcf4`

```dockerfile
```

-	Layers:
	-	`sha256:ccbb0349fdb3825cb42c6a918fcafa7da3f755e9505df67ee490a3e27ede261a`  
		Last Modified: Sat, 07 Sep 2024 14:07:51 GMT  
		Size: 31.0 KB (31004 bytes)  
		MIME: application/vnd.in-toto+json
