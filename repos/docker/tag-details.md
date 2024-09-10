<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.2`](#docker272)
-	[`docker:27.2-cli`](#docker272-cli)
-	[`docker:27.2-dind`](#docker272-dind)
-	[`docker:27.2-dind-rootless`](#docker272-dind-rootless)
-	[`docker:27.2-windowsservercore`](#docker272-windowsservercore)
-	[`docker:27.2-windowsservercore-1809`](#docker272-windowsservercore-1809)
-	[`docker:27.2-windowsservercore-ltsc2022`](#docker272-windowsservercore-ltsc2022)
-	[`docker:27.2.1`](#docker2721)
-	[`docker:27.2.1-alpine3.20`](#docker2721-alpine320)
-	[`docker:27.2.1-cli`](#docker2721-cli)
-	[`docker:27.2.1-cli-alpine3.20`](#docker2721-cli-alpine320)
-	[`docker:27.2.1-dind`](#docker2721-dind)
-	[`docker:27.2.1-dind-alpine3.20`](#docker2721-dind-alpine320)
-	[`docker:27.2.1-dind-rootless`](#docker2721-dind-rootless)
-	[`docker:27.2.1-windowsservercore`](#docker2721-windowsservercore)
-	[`docker:27.2.1-windowsservercore-1809`](#docker2721-windowsservercore-1809)
-	[`docker:27.2.1-windowsservercore-ltsc2022`](#docker2721-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:9cb900abe8b359bdd6a3aa022fee5131fc2a5c7a89478d203a311ac77fc67116
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
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:7792b13addc6ed6a861a7072a423b670420225435d3ce343bd040c891c278636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121147450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0086daff2a557d25daff22a00c4dd8ff328d8f9be542d20e1e8079857388822`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ceed9dcf1fa64d9d597d87991fe2cf573abcdbc71234d48c56934567a0404c`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 16.6 MB (16570446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4f5814a89cb47d5589422329f364480c7f48d77be4e8cd1b8e76bf4f08ce7`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 17.1 MB (17103038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a9997cd15e7365c0b536f26f24b675dc87fb702dac2fd7dc49bc135bf3fea`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 17.8 MB (17771129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309171621269d9bb639255e1d0271bba63d925d3acc913597b8d9375613cadd`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075d49c03c21a287246a41baf7810ed2a633c4559904a18684fdf9d9a47bc5a`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f94772be826fddb813f56152eca2eb28ad9ad36af3396a29893d16edb2458`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c6cec47bdc84ac033aadebeb4278876d3815deb33b86b88fe4db4a756316f`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 6.3 MB (6308146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970185c8f0f65dc61cb7cede5f8398df93a6b4a1d01ec11bf1986d5889cb5b9e`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 84.5 KB (84486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5114dc189d3c23463831fa6fd843435d2272f2ce94b6d3cbcda85fd7c2cdb`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2232ccbfee55d492c7c0158bb5bd9bfcb0b69db3ebe2d61cb18af0a5f9fac67f`  
		Last Modified: Sat, 07 Sep 2024 13:21:33 GMT  
		Size: 53.1 MB (53062898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa12b57340218957a1a92ce8bb0d3704c7d78dfca411cd06e7f96213af3e89`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066bc852ed10399fc3fbd3ae0e8a5a56bf2ecf27e5cdf05aff0f948c4e20276b`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:84adb8e5f65e3226756cd46faf02c7e67f88b94da37b5a9e6c9ebe4ea7ebdeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246b8ab470241ff0a3196b9c199889037c7926685ae82565948df5267df99ffe`

```dockerfile
```

-	Layers:
	-	`sha256:a61a8daec7fe32c2d9aa5f93e31013e0fac92809dd42e7a154d627d3f4335374`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7600dc8fc3557d7ee7a19921a4d8fbe28f56aed480a936dfd9d51592560a330f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122837107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9d41861c64112cb8a31a202d69e0803e0adbd65012ac57b637f37645cbec8f`
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

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:fa9679aabf00703df98795b58f57ee39d82df6fba557562917bdd079c67fc20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db00fd33884626a893016c32ade9c6023eec620dd2a748e706ed90e7f2a493d7`

```dockerfile
```

-	Layers:
	-	`sha256:a1a57225559aee5e90d2a51207bf08c81342d2ee35e16337e1e4825b4bf37d96`  
		Last Modified: Sat, 07 Sep 2024 12:27:45 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:80b0903f5930c71639b172f981c27c99df910c4952c3490d0292a7ef0a5f5dd6
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
$ docker pull docker@sha256:a8edccf86bea036a7144c97b52c7a065c92e210dfaf17b1010e164dcac4d6dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67329838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e672a03560b2a3d6ba369d142ef548b242bff6e2e798c2dfccd327d2fe061bb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc89b6172d3008a561968b5c3fde05195c241defb358e7f44c1a5f925ac666ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301f2e9778e6148772d280399a212b28fa85fe3edded733166c910b916d7e19`

```dockerfile
```

-	Layers:
	-	`sha256:4e4a4094015c54fbd5e500115e79a906383aaa6ca27ee81a1ec8030a44fed0ae`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:725d66887dd4f74f5395ba40d8576da13924b8f0897bef7c4d2ec17555dc9edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62720462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd8483908ae0c4bcbdcd1e6468c90b056ee72e40e3415f57f0d9a39b8309873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:70aa9488ab5f29d5f38298a582ccaf94435b5d35e9a41f6e39062c931427fcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392b0b380e4097563721d5a6b3e05681a27e14e9ea6f38a98e8a45ad83523ff9`

```dockerfile
```

-	Layers:
	-	`sha256:1f99c88a34b63c19c10a1f269233b54de1b3d4e8b1874c81905768fb3f5202c5`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3cc8d15baadfda439faecceaa42fb06010649ab7ad5700ef2063fba0930147d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61749504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7fbf59f98d6c493c0b06f7cccac35aab531e7a2bbb6321746f5b277a3e7340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393b6feaa78b6d4650728d9b69e6f70d27112a6a03406984cbc72a742f26f85`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.1 MB (17103046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87292ec508f8b69c9d1903fe940792d3082bdf92979fa8124624c1f09644d18f`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.8 MB (17771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4710ad5b97391289975ff1885a2f084be2a51196db57c04ce1de0d5dd3a56557`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c52a6e747194908cf3b34d81078babb02155659708d9f529f12da71d46e1ae`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e62303ac844b760938b489c15f98379ae2bbd9f6d20ab325dc15fbb2629cff`  
		Last Modified: Tue, 10 Sep 2024 00:48:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9ca6ba0ac4b0284adce7ef5379d8c694bc3b3e48f63d1a94373a6ed947020370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bdbd0e6ab8542d3b0a5f8638cb6455b15ee4b0066176312fefaf8008787ee6`

```dockerfile
```

-	Layers:
	-	`sha256:5600b47b54b8e3daf423478a38a903cb7dbb8ab255ca1e2c0e6be12bd8c8216d`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68c9aa5db42c4b8b216651a759e12188f7a2b109e793f855198acf85dc7013f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63297534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e796d738d8c403b3a984b5531017ae3fedb59d286339b56dcbd36d65b83b243b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0fea6f0dad6b57714019e4257793003c2d31ac1097da880c674346f209769179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abcc41e8cc1a2782c58d27b175e126708c949800e46cf65e2616e9169dc4476`

```dockerfile
```

-	Layers:
	-	`sha256:ebcf195681f2ed0ac99cacb8e304b38b20e8789bc2903360efd9546bbb7de5a9`  
		Last Modified: Sat, 07 Sep 2024 04:49:05 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:9cb900abe8b359bdd6a3aa022fee5131fc2a5c7a89478d203a311ac77fc67116
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
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7792b13addc6ed6a861a7072a423b670420225435d3ce343bd040c891c278636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121147450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0086daff2a557d25daff22a00c4dd8ff328d8f9be542d20e1e8079857388822`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ceed9dcf1fa64d9d597d87991fe2cf573abcdbc71234d48c56934567a0404c`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 16.6 MB (16570446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4f5814a89cb47d5589422329f364480c7f48d77be4e8cd1b8e76bf4f08ce7`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 17.1 MB (17103038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a9997cd15e7365c0b536f26f24b675dc87fb702dac2fd7dc49bc135bf3fea`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 17.8 MB (17771129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309171621269d9bb639255e1d0271bba63d925d3acc913597b8d9375613cadd`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075d49c03c21a287246a41baf7810ed2a633c4559904a18684fdf9d9a47bc5a`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f94772be826fddb813f56152eca2eb28ad9ad36af3396a29893d16edb2458`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c6cec47bdc84ac033aadebeb4278876d3815deb33b86b88fe4db4a756316f`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 6.3 MB (6308146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970185c8f0f65dc61cb7cede5f8398df93a6b4a1d01ec11bf1986d5889cb5b9e`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 84.5 KB (84486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5114dc189d3c23463831fa6fd843435d2272f2ce94b6d3cbcda85fd7c2cdb`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2232ccbfee55d492c7c0158bb5bd9bfcb0b69db3ebe2d61cb18af0a5f9fac67f`  
		Last Modified: Sat, 07 Sep 2024 13:21:33 GMT  
		Size: 53.1 MB (53062898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa12b57340218957a1a92ce8bb0d3704c7d78dfca411cd06e7f96213af3e89`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066bc852ed10399fc3fbd3ae0e8a5a56bf2ecf27e5cdf05aff0f948c4e20276b`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:84adb8e5f65e3226756cd46faf02c7e67f88b94da37b5a9e6c9ebe4ea7ebdeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246b8ab470241ff0a3196b9c199889037c7926685ae82565948df5267df99ffe`

```dockerfile
```

-	Layers:
	-	`sha256:a61a8daec7fe32c2d9aa5f93e31013e0fac92809dd42e7a154d627d3f4335374`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7600dc8fc3557d7ee7a19921a4d8fbe28f56aed480a936dfd9d51592560a330f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122837107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9d41861c64112cb8a31a202d69e0803e0adbd65012ac57b637f37645cbec8f`
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

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fa9679aabf00703df98795b58f57ee39d82df6fba557562917bdd079c67fc20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db00fd33884626a893016c32ade9c6023eec620dd2a748e706ed90e7f2a493d7`

```dockerfile
```

-	Layers:
	-	`sha256:a1a57225559aee5e90d2a51207bf08c81342d2ee35e16337e1e4825b4bf37d96`  
		Last Modified: Sat, 07 Sep 2024 12:27:45 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:88032762752bc5dbc9e4a175d5ef30e7997ad5d6f6d0e5fc32a6d36fba6e735e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e9322552a4aa517fed3dda0ec83254ce34cb4987b26ff4c6c8aec35f4cb75fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152546039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe67f3218935e737b3eea44ccb93b5d0bd1f962da3e2c5beb8f9e27f6050eed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ddd5be51f440260e6390e8321252731c5a33add50d7de82c0efa08dc2e238`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34748d1a228a91fbe39ac52e1337dfd1ddbb2d1521a49e17fa048f4698f9a40`  
		Last Modified: Fri, 06 Sep 2024 23:15:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e631f15cb81771d7ad3d2e3217eaa2a64cf45f73a9f601ed2292cfd350da79d`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 18.3 MB (18322542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a380a588d9660ddcbbb0bacaa22bd777190c1e522ea0c75624a475709087d94`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 18.4 MB (18404798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d2229981837ef57effc70f7ec87c00a2f95b1335ce3088279d626f36d219a3`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 18.8 MB (18825287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd05ff3e1671337018efda6ccf1ae93c727391b7cd5e57419b976c817c876e0e`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547955fbd3af854e299d3a2d7b1e9cd9d9f1863e1fcbd59ac55302272bb30fb5`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911c38b2b5742aaa23d69b220e80ba2132c3498f3ab11fecb753a523e4472429`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d957e402457f4e5274daafda1f10728a97107f6586cdcbf46d18233065270a4d`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 6.7 MB (6657945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b631605838edb380c436808d30a9b1f1e716a6ead973e471d25f8b2a4a7f82a`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 89.2 KB (89215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47096f94733e316ec172987b32e99af58e318052faa31d97d9cb6e6735b5a869`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8592fececf28720f903d8f934285425bffc06bbd2e6e7c373836e21ee8181968`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 56.8 MB (56779806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dfa20479b7144e474c0fa65d6820de2be77f829d86a5bbef9931a4a0d79515`  
		Last Modified: Sat, 07 Sep 2024 00:08:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53411a209e61e7f105bbad157c41bde5213bf7e9a3c14fef71e57b8df96296fd`  
		Last Modified: Sat, 07 Sep 2024 00:08:09 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef94a2df794a6fcf2fa32f800e1483ee43c35d9d784369ebc17d4fdc7bce5491`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 981.0 KB (980984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99d97e51528fa827a91a5d7a8ac243fa9765f74ff295c65e465c04d5dd825e3`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92868a7da6b20c0ebf58284d6d926190ea119cdce94d71c39e39fded34a44a59`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ae35a318c1c16c6e36992c8d6953987a27341adf640f2e9a2823f5670b057`  
		Last Modified: Sat, 07 Sep 2024 01:05:09 GMT  
		Size: 21.0 MB (20979757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e89de1c33a333da8b1943c167dfd0659eafe125eb4390c3cc66c7d2eace9f`  
		Last Modified: Sat, 07 Sep 2024 01:05:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5317ad6372a5661f4e92ef5cc542fa2ff25cee5fb0334122d931e0580a25d6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd36fd5b1d0f80cccde258ecf4749136a6b297dedaeafee30f640d27589b82`

```dockerfile
```

-	Layers:
	-	`sha256:36e605e724fe9067557b2f2985f445a1cd9c1c52985bb33a7ff35cd9d335b6e1`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
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

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:a37cf925e3846f27b2cd3d336e1fe334c220a2b68eed163466dcf69937559248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:4c8eef37a0c86aa06ad5976c38a052ab7341a1da0d2a517ff066c597e1a2102c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200017471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e9353bddaa42357f13d48483a35ce21c79258551e834702023e0be650aa46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:02:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:02:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332592d922e5dded83a183a722216fbf8d9e16270fa585874df3af5575477ec`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93745372d1a79c87a62454b598858a6f6cc1df8d2be9447cb3d204391ed7d0`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 361.5 KB (361489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6601eeb9638e45c268f11b45669f33c9878b81e18a865f16bc7fd97e985e4ee2`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf3732134bbe550cc9c2e1b8b2c61d7936c1c67a4e30c2cd946c7b085f7460`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679fc02a704b5f3823dc3c6ce6c94090c3b6f3393d34a45c20923b882d691fe`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 18.9 MB (18927866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca67afd286db97657f82fb6017b463e91c31a9b6c95ca07303a34b1d67aef2`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0db3426e28bff54c66b4018a4d03f6f239a2d8ea5308f11a30a59f9b1da54`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfae033be6705adac5640f96e61ba34c52452d7cc66d3db3685bbf1f1578c12`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ed372f37d2e0280f8a8c5f2f6183bf3075554a845fe9e22cb302897ae17f`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 19.3 MB (19257059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3aec99b5a36f7be293d446c07dce9436a71d75b98e743b257a76f3f64c11fa`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5167e8fbb6489585b5ca239706c1c8c7bd7bdf7728fe44e4937491dbb07b6324`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8274b4c972ec015a52de9b8db479c9826c7056fe4ff1173b7be79cca237aea`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfce3c544d708f6342c748468289910bc3f1d4f3e8caf473a55b0d7b0df3dec`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 19.7 MB (19694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:498644c5c8316f5838bb0230478d1d6a6a2d605565f77cee2ce21c0397ba2ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:25fb7b70c8a560f15efbcfd426732a250aa1f0958ca12d86028d74bfb37cd608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:4c8eef37a0c86aa06ad5976c38a052ab7341a1da0d2a517ff066c597e1a2102c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200017471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e9353bddaa42357f13d48483a35ce21c79258551e834702023e0be650aa46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:02:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:02:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332592d922e5dded83a183a722216fbf8d9e16270fa585874df3af5575477ec`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93745372d1a79c87a62454b598858a6f6cc1df8d2be9447cb3d204391ed7d0`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 361.5 KB (361489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6601eeb9638e45c268f11b45669f33c9878b81e18a865f16bc7fd97e985e4ee2`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf3732134bbe550cc9c2e1b8b2c61d7936c1c67a4e30c2cd946c7b085f7460`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679fc02a704b5f3823dc3c6ce6c94090c3b6f3393d34a45c20923b882d691fe`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 18.9 MB (18927866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca67afd286db97657f82fb6017b463e91c31a9b6c95ca07303a34b1d67aef2`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0db3426e28bff54c66b4018a4d03f6f239a2d8ea5308f11a30a59f9b1da54`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfae033be6705adac5640f96e61ba34c52452d7cc66d3db3685bbf1f1578c12`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ed372f37d2e0280f8a8c5f2f6183bf3075554a845fe9e22cb302897ae17f`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 19.3 MB (19257059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3aec99b5a36f7be293d446c07dce9436a71d75b98e743b257a76f3f64c11fa`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5167e8fbb6489585b5ca239706c1c8c7bd7bdf7728fe44e4937491dbb07b6324`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8274b4c972ec015a52de9b8db479c9826c7056fe4ff1173b7be79cca237aea`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfce3c544d708f6342c748468289910bc3f1d4f3e8caf473a55b0d7b0df3dec`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 19.7 MB (19694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2`

```console
$ docker pull docker@sha256:9cb900abe8b359bdd6a3aa022fee5131fc2a5c7a89478d203a311ac77fc67116
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

### `docker:27.2` - linux; amd64

```console
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:7792b13addc6ed6a861a7072a423b670420225435d3ce343bd040c891c278636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121147450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0086daff2a557d25daff22a00c4dd8ff328d8f9be542d20e1e8079857388822`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ceed9dcf1fa64d9d597d87991fe2cf573abcdbc71234d48c56934567a0404c`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 16.6 MB (16570446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4f5814a89cb47d5589422329f364480c7f48d77be4e8cd1b8e76bf4f08ce7`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 17.1 MB (17103038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a9997cd15e7365c0b536f26f24b675dc87fb702dac2fd7dc49bc135bf3fea`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 17.8 MB (17771129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309171621269d9bb639255e1d0271bba63d925d3acc913597b8d9375613cadd`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075d49c03c21a287246a41baf7810ed2a633c4559904a18684fdf9d9a47bc5a`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f94772be826fddb813f56152eca2eb28ad9ad36af3396a29893d16edb2458`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c6cec47bdc84ac033aadebeb4278876d3815deb33b86b88fe4db4a756316f`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 6.3 MB (6308146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970185c8f0f65dc61cb7cede5f8398df93a6b4a1d01ec11bf1986d5889cb5b9e`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 84.5 KB (84486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5114dc189d3c23463831fa6fd843435d2272f2ce94b6d3cbcda85fd7c2cdb`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2232ccbfee55d492c7c0158bb5bd9bfcb0b69db3ebe2d61cb18af0a5f9fac67f`  
		Last Modified: Sat, 07 Sep 2024 13:21:33 GMT  
		Size: 53.1 MB (53062898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa12b57340218957a1a92ce8bb0d3704c7d78dfca411cd06e7f96213af3e89`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066bc852ed10399fc3fbd3ae0e8a5a56bf2ecf27e5cdf05aff0f948c4e20276b`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:84adb8e5f65e3226756cd46faf02c7e67f88b94da37b5a9e6c9ebe4ea7ebdeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246b8ab470241ff0a3196b9c199889037c7926685ae82565948df5267df99ffe`

```dockerfile
```

-	Layers:
	-	`sha256:a61a8daec7fe32c2d9aa5f93e31013e0fac92809dd42e7a154d627d3f4335374`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7600dc8fc3557d7ee7a19921a4d8fbe28f56aed480a936dfd9d51592560a330f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122837107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9d41861c64112cb8a31a202d69e0803e0adbd65012ac57b637f37645cbec8f`
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

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:fa9679aabf00703df98795b58f57ee39d82df6fba557562917bdd079c67fc20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db00fd33884626a893016c32ade9c6023eec620dd2a748e706ed90e7f2a493d7`

```dockerfile
```

-	Layers:
	-	`sha256:a1a57225559aee5e90d2a51207bf08c81342d2ee35e16337e1e4825b4bf37d96`  
		Last Modified: Sat, 07 Sep 2024 12:27:45 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2-cli`

```console
$ docker pull docker@sha256:80b0903f5930c71639b172f981c27c99df910c4952c3490d0292a7ef0a5f5dd6
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

### `docker:27.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:a8edccf86bea036a7144c97b52c7a065c92e210dfaf17b1010e164dcac4d6dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67329838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e672a03560b2a3d6ba369d142ef548b242bff6e2e798c2dfccd327d2fe061bb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc89b6172d3008a561968b5c3fde05195c241defb358e7f44c1a5f925ac666ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301f2e9778e6148772d280399a212b28fa85fe3edded733166c910b916d7e19`

```dockerfile
```

-	Layers:
	-	`sha256:4e4a4094015c54fbd5e500115e79a906383aaa6ca27ee81a1ec8030a44fed0ae`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:725d66887dd4f74f5395ba40d8576da13924b8f0897bef7c4d2ec17555dc9edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62720462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd8483908ae0c4bcbdcd1e6468c90b056ee72e40e3415f57f0d9a39b8309873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:70aa9488ab5f29d5f38298a582ccaf94435b5d35e9a41f6e39062c931427fcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392b0b380e4097563721d5a6b3e05681a27e14e9ea6f38a98e8a45ad83523ff9`

```dockerfile
```

-	Layers:
	-	`sha256:1f99c88a34b63c19c10a1f269233b54de1b3d4e8b1874c81905768fb3f5202c5`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3cc8d15baadfda439faecceaa42fb06010649ab7ad5700ef2063fba0930147d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61749504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7fbf59f98d6c493c0b06f7cccac35aab531e7a2bbb6321746f5b277a3e7340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393b6feaa78b6d4650728d9b69e6f70d27112a6a03406984cbc72a742f26f85`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.1 MB (17103046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87292ec508f8b69c9d1903fe940792d3082bdf92979fa8124624c1f09644d18f`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.8 MB (17771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4710ad5b97391289975ff1885a2f084be2a51196db57c04ce1de0d5dd3a56557`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c52a6e747194908cf3b34d81078babb02155659708d9f529f12da71d46e1ae`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e62303ac844b760938b489c15f98379ae2bbd9f6d20ab325dc15fbb2629cff`  
		Last Modified: Tue, 10 Sep 2024 00:48:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9ca6ba0ac4b0284adce7ef5379d8c694bc3b3e48f63d1a94373a6ed947020370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bdbd0e6ab8542d3b0a5f8638cb6455b15ee4b0066176312fefaf8008787ee6`

```dockerfile
```

-	Layers:
	-	`sha256:5600b47b54b8e3daf423478a38a903cb7dbb8ab255ca1e2c0e6be12bd8c8216d`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68c9aa5db42c4b8b216651a759e12188f7a2b109e793f855198acf85dc7013f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63297534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e796d738d8c403b3a984b5531017ae3fedb59d286339b56dcbd36d65b83b243b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0fea6f0dad6b57714019e4257793003c2d31ac1097da880c674346f209769179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abcc41e8cc1a2782c58d27b175e126708c949800e46cf65e2616e9169dc4476`

```dockerfile
```

-	Layers:
	-	`sha256:ebcf195681f2ed0ac99cacb8e304b38b20e8789bc2903360efd9546bbb7de5a9`  
		Last Modified: Sat, 07 Sep 2024 04:49:05 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2-dind`

```console
$ docker pull docker@sha256:9cb900abe8b359bdd6a3aa022fee5131fc2a5c7a89478d203a311ac77fc67116
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

### `docker:27.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7792b13addc6ed6a861a7072a423b670420225435d3ce343bd040c891c278636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121147450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0086daff2a557d25daff22a00c4dd8ff328d8f9be542d20e1e8079857388822`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ceed9dcf1fa64d9d597d87991fe2cf573abcdbc71234d48c56934567a0404c`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 16.6 MB (16570446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4f5814a89cb47d5589422329f364480c7f48d77be4e8cd1b8e76bf4f08ce7`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 17.1 MB (17103038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a9997cd15e7365c0b536f26f24b675dc87fb702dac2fd7dc49bc135bf3fea`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 17.8 MB (17771129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309171621269d9bb639255e1d0271bba63d925d3acc913597b8d9375613cadd`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075d49c03c21a287246a41baf7810ed2a633c4559904a18684fdf9d9a47bc5a`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f94772be826fddb813f56152eca2eb28ad9ad36af3396a29893d16edb2458`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c6cec47bdc84ac033aadebeb4278876d3815deb33b86b88fe4db4a756316f`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 6.3 MB (6308146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970185c8f0f65dc61cb7cede5f8398df93a6b4a1d01ec11bf1986d5889cb5b9e`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 84.5 KB (84486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5114dc189d3c23463831fa6fd843435d2272f2ce94b6d3cbcda85fd7c2cdb`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2232ccbfee55d492c7c0158bb5bd9bfcb0b69db3ebe2d61cb18af0a5f9fac67f`  
		Last Modified: Sat, 07 Sep 2024 13:21:33 GMT  
		Size: 53.1 MB (53062898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa12b57340218957a1a92ce8bb0d3704c7d78dfca411cd06e7f96213af3e89`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066bc852ed10399fc3fbd3ae0e8a5a56bf2ecf27e5cdf05aff0f948c4e20276b`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:84adb8e5f65e3226756cd46faf02c7e67f88b94da37b5a9e6c9ebe4ea7ebdeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246b8ab470241ff0a3196b9c199889037c7926685ae82565948df5267df99ffe`

```dockerfile
```

-	Layers:
	-	`sha256:a61a8daec7fe32c2d9aa5f93e31013e0fac92809dd42e7a154d627d3f4335374`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7600dc8fc3557d7ee7a19921a4d8fbe28f56aed480a936dfd9d51592560a330f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122837107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9d41861c64112cb8a31a202d69e0803e0adbd65012ac57b637f37645cbec8f`
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

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fa9679aabf00703df98795b58f57ee39d82df6fba557562917bdd079c67fc20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db00fd33884626a893016c32ade9c6023eec620dd2a748e706ed90e7f2a493d7`

```dockerfile
```

-	Layers:
	-	`sha256:a1a57225559aee5e90d2a51207bf08c81342d2ee35e16337e1e4825b4bf37d96`  
		Last Modified: Sat, 07 Sep 2024 12:27:45 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2-dind-rootless`

```console
$ docker pull docker@sha256:88032762752bc5dbc9e4a175d5ef30e7997ad5d6f6d0e5fc32a6d36fba6e735e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e9322552a4aa517fed3dda0ec83254ce34cb4987b26ff4c6c8aec35f4cb75fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152546039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe67f3218935e737b3eea44ccb93b5d0bd1f962da3e2c5beb8f9e27f6050eed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ddd5be51f440260e6390e8321252731c5a33add50d7de82c0efa08dc2e238`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34748d1a228a91fbe39ac52e1337dfd1ddbb2d1521a49e17fa048f4698f9a40`  
		Last Modified: Fri, 06 Sep 2024 23:15:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e631f15cb81771d7ad3d2e3217eaa2a64cf45f73a9f601ed2292cfd350da79d`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 18.3 MB (18322542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a380a588d9660ddcbbb0bacaa22bd777190c1e522ea0c75624a475709087d94`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 18.4 MB (18404798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d2229981837ef57effc70f7ec87c00a2f95b1335ce3088279d626f36d219a3`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 18.8 MB (18825287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd05ff3e1671337018efda6ccf1ae93c727391b7cd5e57419b976c817c876e0e`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547955fbd3af854e299d3a2d7b1e9cd9d9f1863e1fcbd59ac55302272bb30fb5`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911c38b2b5742aaa23d69b220e80ba2132c3498f3ab11fecb753a523e4472429`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d957e402457f4e5274daafda1f10728a97107f6586cdcbf46d18233065270a4d`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 6.7 MB (6657945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b631605838edb380c436808d30a9b1f1e716a6ead973e471d25f8b2a4a7f82a`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 89.2 KB (89215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47096f94733e316ec172987b32e99af58e318052faa31d97d9cb6e6735b5a869`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8592fececf28720f903d8f934285425bffc06bbd2e6e7c373836e21ee8181968`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 56.8 MB (56779806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dfa20479b7144e474c0fa65d6820de2be77f829d86a5bbef9931a4a0d79515`  
		Last Modified: Sat, 07 Sep 2024 00:08:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53411a209e61e7f105bbad157c41bde5213bf7e9a3c14fef71e57b8df96296fd`  
		Last Modified: Sat, 07 Sep 2024 00:08:09 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef94a2df794a6fcf2fa32f800e1483ee43c35d9d784369ebc17d4fdc7bce5491`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 981.0 KB (980984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99d97e51528fa827a91a5d7a8ac243fa9765f74ff295c65e465c04d5dd825e3`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92868a7da6b20c0ebf58284d6d926190ea119cdce94d71c39e39fded34a44a59`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ae35a318c1c16c6e36992c8d6953987a27341adf640f2e9a2823f5670b057`  
		Last Modified: Sat, 07 Sep 2024 01:05:09 GMT  
		Size: 21.0 MB (20979757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e89de1c33a333da8b1943c167dfd0659eafe125eb4390c3cc66c7d2eace9f`  
		Last Modified: Sat, 07 Sep 2024 01:05:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5317ad6372a5661f4e92ef5cc542fa2ff25cee5fb0334122d931e0580a25d6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd36fd5b1d0f80cccde258ecf4749136a6b297dedaeafee30f640d27589b82`

```dockerfile
```

-	Layers:
	-	`sha256:36e605e724fe9067557b2f2985f445a1cd9c1c52985bb33a7ff35cd9d335b6e1`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind-rootless` - linux; arm64 variant v8

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

### `docker:27.2-dind-rootless` - unknown; unknown

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

## `docker:27.2-windowsservercore`

```console
$ docker pull docker@sha256:a37cf925e3846f27b2cd3d336e1fe334c220a2b68eed163466dcf69937559248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27.2-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:4c8eef37a0c86aa06ad5976c38a052ab7341a1da0d2a517ff066c597e1a2102c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200017471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e9353bddaa42357f13d48483a35ce21c79258551e834702023e0be650aa46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:02:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:02:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332592d922e5dded83a183a722216fbf8d9e16270fa585874df3af5575477ec`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93745372d1a79c87a62454b598858a6f6cc1df8d2be9447cb3d204391ed7d0`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 361.5 KB (361489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6601eeb9638e45c268f11b45669f33c9878b81e18a865f16bc7fd97e985e4ee2`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf3732134bbe550cc9c2e1b8b2c61d7936c1c67a4e30c2cd946c7b085f7460`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679fc02a704b5f3823dc3c6ce6c94090c3b6f3393d34a45c20923b882d691fe`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 18.9 MB (18927866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca67afd286db97657f82fb6017b463e91c31a9b6c95ca07303a34b1d67aef2`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0db3426e28bff54c66b4018a4d03f6f239a2d8ea5308f11a30a59f9b1da54`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfae033be6705adac5640f96e61ba34c52452d7cc66d3db3685bbf1f1578c12`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ed372f37d2e0280f8a8c5f2f6183bf3075554a845fe9e22cb302897ae17f`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 19.3 MB (19257059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3aec99b5a36f7be293d446c07dce9436a71d75b98e743b257a76f3f64c11fa`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5167e8fbb6489585b5ca239706c1c8c7bd7bdf7728fe44e4937491dbb07b6324`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8274b4c972ec015a52de9b8db479c9826c7056fe4ff1173b7be79cca237aea`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfce3c544d708f6342c748468289910bc3f1d4f3e8caf473a55b0d7b0df3dec`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 19.7 MB (19694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.2-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2-windowsservercore-1809`

```console
$ docker pull docker@sha256:498644c5c8316f5838bb0230478d1d6a6a2d605565f77cee2ce21c0397ba2ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27.2-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:25fb7b70c8a560f15efbcfd426732a250aa1f0958ca12d86028d74bfb37cd608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27.2-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:4c8eef37a0c86aa06ad5976c38a052ab7341a1da0d2a517ff066c597e1a2102c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200017471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e9353bddaa42357f13d48483a35ce21c79258551e834702023e0be650aa46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:02:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:02:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332592d922e5dded83a183a722216fbf8d9e16270fa585874df3af5575477ec`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93745372d1a79c87a62454b598858a6f6cc1df8d2be9447cb3d204391ed7d0`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 361.5 KB (361489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6601eeb9638e45c268f11b45669f33c9878b81e18a865f16bc7fd97e985e4ee2`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf3732134bbe550cc9c2e1b8b2c61d7936c1c67a4e30c2cd946c7b085f7460`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679fc02a704b5f3823dc3c6ce6c94090c3b6f3393d34a45c20923b882d691fe`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 18.9 MB (18927866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca67afd286db97657f82fb6017b463e91c31a9b6c95ca07303a34b1d67aef2`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0db3426e28bff54c66b4018a4d03f6f239a2d8ea5308f11a30a59f9b1da54`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfae033be6705adac5640f96e61ba34c52452d7cc66d3db3685bbf1f1578c12`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ed372f37d2e0280f8a8c5f2f6183bf3075554a845fe9e22cb302897ae17f`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 19.3 MB (19257059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3aec99b5a36f7be293d446c07dce9436a71d75b98e743b257a76f3f64c11fa`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5167e8fbb6489585b5ca239706c1c8c7bd7bdf7728fe44e4937491dbb07b6324`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8274b4c972ec015a52de9b8db479c9826c7056fe4ff1173b7be79cca237aea`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfce3c544d708f6342c748468289910bc3f1d4f3e8caf473a55b0d7b0df3dec`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 19.7 MB (19694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.1`

```console
$ docker pull docker@sha256:eb6308292ccf83461f26dd755a53802d9952eece22111602662cd86d3fa4590d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:27.2.1` - linux; amd64

```console
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:27.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-alpine3.20`

```console
$ docker pull docker@sha256:eb6308292ccf83461f26dd755a53802d9952eece22111602662cd86d3fa4590d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:27.2.1-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:27.2.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-cli`

```console
$ docker pull docker@sha256:d70f9fa08e518ba2cf6d3fd40b7249e31b5125b73322de43f9820304a1185388
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `docker:27.2.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:a8edccf86bea036a7144c97b52c7a065c92e210dfaf17b1010e164dcac4d6dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67329838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e672a03560b2a3d6ba369d142ef548b242bff6e2e798c2dfccd327d2fe061bb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc89b6172d3008a561968b5c3fde05195c241defb358e7f44c1a5f925ac666ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301f2e9778e6148772d280399a212b28fa85fe3edded733166c910b916d7e19`

```dockerfile
```

-	Layers:
	-	`sha256:4e4a4094015c54fbd5e500115e79a906383aaa6ca27ee81a1ec8030a44fed0ae`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:725d66887dd4f74f5395ba40d8576da13924b8f0897bef7c4d2ec17555dc9edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62720462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd8483908ae0c4bcbdcd1e6468c90b056ee72e40e3415f57f0d9a39b8309873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:70aa9488ab5f29d5f38298a582ccaf94435b5d35e9a41f6e39062c931427fcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392b0b380e4097563721d5a6b3e05681a27e14e9ea6f38a98e8a45ad83523ff9`

```dockerfile
```

-	Layers:
	-	`sha256:1f99c88a34b63c19c10a1f269233b54de1b3d4e8b1874c81905768fb3f5202c5`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3cc8d15baadfda439faecceaa42fb06010649ab7ad5700ef2063fba0930147d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61749504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7fbf59f98d6c493c0b06f7cccac35aab531e7a2bbb6321746f5b277a3e7340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393b6feaa78b6d4650728d9b69e6f70d27112a6a03406984cbc72a742f26f85`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.1 MB (17103046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87292ec508f8b69c9d1903fe940792d3082bdf92979fa8124624c1f09644d18f`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.8 MB (17771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4710ad5b97391289975ff1885a2f084be2a51196db57c04ce1de0d5dd3a56557`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c52a6e747194908cf3b34d81078babb02155659708d9f529f12da71d46e1ae`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e62303ac844b760938b489c15f98379ae2bbd9f6d20ab325dc15fbb2629cff`  
		Last Modified: Tue, 10 Sep 2024 00:48:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9ca6ba0ac4b0284adce7ef5379d8c694bc3b3e48f63d1a94373a6ed947020370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bdbd0e6ab8542d3b0a5f8638cb6455b15ee4b0066176312fefaf8008787ee6`

```dockerfile
```

-	Layers:
	-	`sha256:5600b47b54b8e3daf423478a38a903cb7dbb8ab255ca1e2c0e6be12bd8c8216d`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-cli-alpine3.20`

```console
$ docker pull docker@sha256:d70f9fa08e518ba2cf6d3fd40b7249e31b5125b73322de43f9820304a1185388
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `docker:27.2.1-cli-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:a8edccf86bea036a7144c97b52c7a065c92e210dfaf17b1010e164dcac4d6dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67329838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e672a03560b2a3d6ba369d142ef548b242bff6e2e798c2dfccd327d2fe061bb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:dc89b6172d3008a561968b5c3fde05195c241defb358e7f44c1a5f925ac666ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301f2e9778e6148772d280399a212b28fa85fe3edded733166c910b916d7e19`

```dockerfile
```

-	Layers:
	-	`sha256:4e4a4094015c54fbd5e500115e79a906383aaa6ca27ee81a1ec8030a44fed0ae`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:725d66887dd4f74f5395ba40d8576da13924b8f0897bef7c4d2ec17555dc9edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62720462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd8483908ae0c4bcbdcd1e6468c90b056ee72e40e3415f57f0d9a39b8309873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:70aa9488ab5f29d5f38298a582ccaf94435b5d35e9a41f6e39062c931427fcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392b0b380e4097563721d5a6b3e05681a27e14e9ea6f38a98e8a45ad83523ff9`

```dockerfile
```

-	Layers:
	-	`sha256:1f99c88a34b63c19c10a1f269233b54de1b3d4e8b1874c81905768fb3f5202c5`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:3cc8d15baadfda439faecceaa42fb06010649ab7ad5700ef2063fba0930147d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61749504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7fbf59f98d6c493c0b06f7cccac35aab531e7a2bbb6321746f5b277a3e7340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393b6feaa78b6d4650728d9b69e6f70d27112a6a03406984cbc72a742f26f85`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.1 MB (17103046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87292ec508f8b69c9d1903fe940792d3082bdf92979fa8124624c1f09644d18f`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.8 MB (17771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4710ad5b97391289975ff1885a2f084be2a51196db57c04ce1de0d5dd3a56557`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c52a6e747194908cf3b34d81078babb02155659708d9f529f12da71d46e1ae`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e62303ac844b760938b489c15f98379ae2bbd9f6d20ab325dc15fbb2629cff`  
		Last Modified: Tue, 10 Sep 2024 00:48:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:9ca6ba0ac4b0284adce7ef5379d8c694bc3b3e48f63d1a94373a6ed947020370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bdbd0e6ab8542d3b0a5f8638cb6455b15ee4b0066176312fefaf8008787ee6`

```dockerfile
```

-	Layers:
	-	`sha256:5600b47b54b8e3daf423478a38a903cb7dbb8ab255ca1e2c0e6be12bd8c8216d`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-dind`

```console
$ docker pull docker@sha256:eb6308292ccf83461f26dd755a53802d9952eece22111602662cd86d3fa4590d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:27.2.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:27.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-dind-alpine3.20`

```console
$ docker pull docker@sha256:eb6308292ccf83461f26dd755a53802d9952eece22111602662cd86d3fa4590d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:27.2.1-dind-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:27.2.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.2.1-windowsservercore`

```console
$ docker pull docker@sha256:a37cf925e3846f27b2cd3d336e1fe334c220a2b68eed163466dcf69937559248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27.2.1-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:4c8eef37a0c86aa06ad5976c38a052ab7341a1da0d2a517ff066c597e1a2102c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200017471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e9353bddaa42357f13d48483a35ce21c79258551e834702023e0be650aa46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:02:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:02:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332592d922e5dded83a183a722216fbf8d9e16270fa585874df3af5575477ec`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93745372d1a79c87a62454b598858a6f6cc1df8d2be9447cb3d204391ed7d0`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 361.5 KB (361489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6601eeb9638e45c268f11b45669f33c9878b81e18a865f16bc7fd97e985e4ee2`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf3732134bbe550cc9c2e1b8b2c61d7936c1c67a4e30c2cd946c7b085f7460`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679fc02a704b5f3823dc3c6ce6c94090c3b6f3393d34a45c20923b882d691fe`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 18.9 MB (18927866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca67afd286db97657f82fb6017b463e91c31a9b6c95ca07303a34b1d67aef2`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0db3426e28bff54c66b4018a4d03f6f239a2d8ea5308f11a30a59f9b1da54`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfae033be6705adac5640f96e61ba34c52452d7cc66d3db3685bbf1f1578c12`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ed372f37d2e0280f8a8c5f2f6183bf3075554a845fe9e22cb302897ae17f`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 19.3 MB (19257059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3aec99b5a36f7be293d446c07dce9436a71d75b98e743b257a76f3f64c11fa`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5167e8fbb6489585b5ca239706c1c8c7bd7bdf7728fe44e4937491dbb07b6324`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8274b4c972ec015a52de9b8db479c9826c7056fe4ff1173b7be79cca237aea`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfce3c544d708f6342c748468289910bc3f1d4f3e8caf473a55b0d7b0df3dec`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 19.7 MB (19694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.2.1-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:498644c5c8316f5838bb0230478d1d6a6a2d605565f77cee2ce21c0397ba2ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27.2.1-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:25fb7b70c8a560f15efbcfd426732a250aa1f0958ca12d86028d74bfb37cd608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27.2.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:4c8eef37a0c86aa06ad5976c38a052ab7341a1da0d2a517ff066c597e1a2102c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200017471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e9353bddaa42357f13d48483a35ce21c79258551e834702023e0be650aa46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:02:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:02:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332592d922e5dded83a183a722216fbf8d9e16270fa585874df3af5575477ec`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93745372d1a79c87a62454b598858a6f6cc1df8d2be9447cb3d204391ed7d0`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 361.5 KB (361489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6601eeb9638e45c268f11b45669f33c9878b81e18a865f16bc7fd97e985e4ee2`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf3732134bbe550cc9c2e1b8b2c61d7936c1c67a4e30c2cd946c7b085f7460`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679fc02a704b5f3823dc3c6ce6c94090c3b6f3393d34a45c20923b882d691fe`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 18.9 MB (18927866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca67afd286db97657f82fb6017b463e91c31a9b6c95ca07303a34b1d67aef2`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0db3426e28bff54c66b4018a4d03f6f239a2d8ea5308f11a30a59f9b1da54`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfae033be6705adac5640f96e61ba34c52452d7cc66d3db3685bbf1f1578c12`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ed372f37d2e0280f8a8c5f2f6183bf3075554a845fe9e22cb302897ae17f`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 19.3 MB (19257059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3aec99b5a36f7be293d446c07dce9436a71d75b98e743b257a76f3f64c11fa`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5167e8fbb6489585b5ca239706c1c8c7bd7bdf7728fe44e4937491dbb07b6324`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8274b4c972ec015a52de9b8db479c9826c7056fe4ff1173b7be79cca237aea`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfce3c544d708f6342c748468289910bc3f1d4f3e8caf473a55b0d7b0df3dec`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 19.7 MB (19694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:80b0903f5930c71639b172f981c27c99df910c4952c3490d0292a7ef0a5f5dd6
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
$ docker pull docker@sha256:a8edccf86bea036a7144c97b52c7a065c92e210dfaf17b1010e164dcac4d6dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67329838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e672a03560b2a3d6ba369d142ef548b242bff6e2e798c2dfccd327d2fe061bb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc89b6172d3008a561968b5c3fde05195c241defb358e7f44c1a5f925ac666ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301f2e9778e6148772d280399a212b28fa85fe3edded733166c910b916d7e19`

```dockerfile
```

-	Layers:
	-	`sha256:4e4a4094015c54fbd5e500115e79a906383aaa6ca27ee81a1ec8030a44fed0ae`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:725d66887dd4f74f5395ba40d8576da13924b8f0897bef7c4d2ec17555dc9edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62720462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd8483908ae0c4bcbdcd1e6468c90b056ee72e40e3415f57f0d9a39b8309873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:70aa9488ab5f29d5f38298a582ccaf94435b5d35e9a41f6e39062c931427fcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392b0b380e4097563721d5a6b3e05681a27e14e9ea6f38a98e8a45ad83523ff9`

```dockerfile
```

-	Layers:
	-	`sha256:1f99c88a34b63c19c10a1f269233b54de1b3d4e8b1874c81905768fb3f5202c5`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3cc8d15baadfda439faecceaa42fb06010649ab7ad5700ef2063fba0930147d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61749504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7fbf59f98d6c493c0b06f7cccac35aab531e7a2bbb6321746f5b277a3e7340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393b6feaa78b6d4650728d9b69e6f70d27112a6a03406984cbc72a742f26f85`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.1 MB (17103046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87292ec508f8b69c9d1903fe940792d3082bdf92979fa8124624c1f09644d18f`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 17.8 MB (17771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4710ad5b97391289975ff1885a2f084be2a51196db57c04ce1de0d5dd3a56557`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c52a6e747194908cf3b34d81078babb02155659708d9f529f12da71d46e1ae`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e62303ac844b760938b489c15f98379ae2bbd9f6d20ab325dc15fbb2629cff`  
		Last Modified: Tue, 10 Sep 2024 00:48:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:9ca6ba0ac4b0284adce7ef5379d8c694bc3b3e48f63d1a94373a6ed947020370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bdbd0e6ab8542d3b0a5f8638cb6455b15ee4b0066176312fefaf8008787ee6`

```dockerfile
```

-	Layers:
	-	`sha256:5600b47b54b8e3daf423478a38a903cb7dbb8ab255ca1e2c0e6be12bd8c8216d`  
		Last Modified: Tue, 10 Sep 2024 00:48:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68c9aa5db42c4b8b216651a759e12188f7a2b109e793f855198acf85dc7013f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63297534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e796d738d8c403b3a984b5531017ae3fedb59d286339b56dcbd36d65b83b243b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0fea6f0dad6b57714019e4257793003c2d31ac1097da880c674346f209769179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abcc41e8cc1a2782c58d27b175e126708c949800e46cf65e2616e9169dc4476`

```dockerfile
```

-	Layers:
	-	`sha256:ebcf195681f2ed0ac99cacb8e304b38b20e8789bc2903360efd9546bbb7de5a9`  
		Last Modified: Sat, 07 Sep 2024 04:49:05 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:9cb900abe8b359bdd6a3aa022fee5131fc2a5c7a89478d203a311ac77fc67116
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
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7792b13addc6ed6a861a7072a423b670420225435d3ce343bd040c891c278636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121147450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0086daff2a557d25daff22a00c4dd8ff328d8f9be542d20e1e8079857388822`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ceed9dcf1fa64d9d597d87991fe2cf573abcdbc71234d48c56934567a0404c`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 16.6 MB (16570446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4f5814a89cb47d5589422329f364480c7f48d77be4e8cd1b8e76bf4f08ce7`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 17.1 MB (17103038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a9997cd15e7365c0b536f26f24b675dc87fb702dac2fd7dc49bc135bf3fea`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 17.8 MB (17771129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309171621269d9bb639255e1d0271bba63d925d3acc913597b8d9375613cadd`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075d49c03c21a287246a41baf7810ed2a633c4559904a18684fdf9d9a47bc5a`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f94772be826fddb813f56152eca2eb28ad9ad36af3396a29893d16edb2458`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c6cec47bdc84ac033aadebeb4278876d3815deb33b86b88fe4db4a756316f`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 6.3 MB (6308146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970185c8f0f65dc61cb7cede5f8398df93a6b4a1d01ec11bf1986d5889cb5b9e`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 84.5 KB (84486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5114dc189d3c23463831fa6fd843435d2272f2ce94b6d3cbcda85fd7c2cdb`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2232ccbfee55d492c7c0158bb5bd9bfcb0b69db3ebe2d61cb18af0a5f9fac67f`  
		Last Modified: Sat, 07 Sep 2024 13:21:33 GMT  
		Size: 53.1 MB (53062898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa12b57340218957a1a92ce8bb0d3704c7d78dfca411cd06e7f96213af3e89`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066bc852ed10399fc3fbd3ae0e8a5a56bf2ecf27e5cdf05aff0f948c4e20276b`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:84adb8e5f65e3226756cd46faf02c7e67f88b94da37b5a9e6c9ebe4ea7ebdeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246b8ab470241ff0a3196b9c199889037c7926685ae82565948df5267df99ffe`

```dockerfile
```

-	Layers:
	-	`sha256:a61a8daec7fe32c2d9aa5f93e31013e0fac92809dd42e7a154d627d3f4335374`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7600dc8fc3557d7ee7a19921a4d8fbe28f56aed480a936dfd9d51592560a330f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122837107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9d41861c64112cb8a31a202d69e0803e0adbd65012ac57b637f37645cbec8f`
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:fa9679aabf00703df98795b58f57ee39d82df6fba557562917bdd079c67fc20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db00fd33884626a893016c32ade9c6023eec620dd2a748e706ed90e7f2a493d7`

```dockerfile
```

-	Layers:
	-	`sha256:a1a57225559aee5e90d2a51207bf08c81342d2ee35e16337e1e4825b4bf37d96`  
		Last Modified: Sat, 07 Sep 2024 12:27:45 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:88032762752bc5dbc9e4a175d5ef30e7997ad5d6f6d0e5fc32a6d36fba6e735e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e9322552a4aa517fed3dda0ec83254ce34cb4987b26ff4c6c8aec35f4cb75fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152546039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe67f3218935e737b3eea44ccb93b5d0bd1f962da3e2c5beb8f9e27f6050eed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ddd5be51f440260e6390e8321252731c5a33add50d7de82c0efa08dc2e238`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34748d1a228a91fbe39ac52e1337dfd1ddbb2d1521a49e17fa048f4698f9a40`  
		Last Modified: Fri, 06 Sep 2024 23:15:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e631f15cb81771d7ad3d2e3217eaa2a64cf45f73a9f601ed2292cfd350da79d`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 18.3 MB (18322542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a380a588d9660ddcbbb0bacaa22bd777190c1e522ea0c75624a475709087d94`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 18.4 MB (18404798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d2229981837ef57effc70f7ec87c00a2f95b1335ce3088279d626f36d219a3`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 18.8 MB (18825287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd05ff3e1671337018efda6ccf1ae93c727391b7cd5e57419b976c817c876e0e`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547955fbd3af854e299d3a2d7b1e9cd9d9f1863e1fcbd59ac55302272bb30fb5`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911c38b2b5742aaa23d69b220e80ba2132c3498f3ab11fecb753a523e4472429`  
		Last Modified: Fri, 06 Sep 2024 23:15:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d957e402457f4e5274daafda1f10728a97107f6586cdcbf46d18233065270a4d`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 6.7 MB (6657945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b631605838edb380c436808d30a9b1f1e716a6ead973e471d25f8b2a4a7f82a`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 89.2 KB (89215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47096f94733e316ec172987b32e99af58e318052faa31d97d9cb6e6735b5a869`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8592fececf28720f903d8f934285425bffc06bbd2e6e7c373836e21ee8181968`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 56.8 MB (56779806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dfa20479b7144e474c0fa65d6820de2be77f829d86a5bbef9931a4a0d79515`  
		Last Modified: Sat, 07 Sep 2024 00:08:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53411a209e61e7f105bbad157c41bde5213bf7e9a3c14fef71e57b8df96296fd`  
		Last Modified: Sat, 07 Sep 2024 00:08:09 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef94a2df794a6fcf2fa32f800e1483ee43c35d9d784369ebc17d4fdc7bce5491`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 981.0 KB (980984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99d97e51528fa827a91a5d7a8ac243fa9765f74ff295c65e465c04d5dd825e3`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92868a7da6b20c0ebf58284d6d926190ea119cdce94d71c39e39fded34a44a59`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ae35a318c1c16c6e36992c8d6953987a27341adf640f2e9a2823f5670b057`  
		Last Modified: Sat, 07 Sep 2024 01:05:09 GMT  
		Size: 21.0 MB (20979757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e89de1c33a333da8b1943c167dfd0659eafe125eb4390c3cc66c7d2eace9f`  
		Last Modified: Sat, 07 Sep 2024 01:05:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5317ad6372a5661f4e92ef5cc542fa2ff25cee5fb0334122d931e0580a25d6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd36fd5b1d0f80cccde258ecf4749136a6b297dedaeafee30f640d27589b82`

```dockerfile
```

-	Layers:
	-	`sha256:36e605e724fe9067557b2f2985f445a1cd9c1c52985bb33a7ff35cd9d335b6e1`  
		Last Modified: Sat, 07 Sep 2024 01:05:08 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

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

### `docker:dind-rootless` - unknown; unknown

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

## `docker:latest`

```console
$ docker pull docker@sha256:9cb900abe8b359bdd6a3aa022fee5131fc2a5c7a89478d203a311ac77fc67116
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
$ docker pull docker@sha256:9ae7a2cc38a6341ff672b7a54bcd143b55086fed0504a7778414630c6c8d59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131856216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1a38c65d43571c3effdca29ce347ba7d82c3a94741d517b07fd721b4e2b59`
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:873b2aa96ec80b85623c85a09a5384db0ef3389c93485d1fd19d4f493f7a06b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6e3f8fdaa6b1faa1fe8c79eb59f19d81ac4b56b0e49958edb666da29bddf8e`

```dockerfile
```

-	Layers:
	-	`sha256:34f62db0cd6677fae6e3cce6843335d96885a910beb1e3fe70e251a56cb97f39`  
		Last Modified: Mon, 09 Sep 2024 23:53:42 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:9fa6bf335ba2d1e3830131b642b9c4bd0e9aff39bf0526d686072a75fb362f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123293087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4806032558cd4867f39c303de3e124d9c40148b98bc3305ddfe4d0f3101172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a6da3f481a8af3db38d48916fc247fee3eff19410fe2eba020cec44829231`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.1 MB (17114714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a726626efc2c69d82da60cb97999292ab5839894f0051e21a5c44aba369fefa`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 17.8 MB (17783315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46167fb9275e6f4d311ff2242aa5bf59314a77cfda83aaae185abd287bc6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce24a6c35c24420491a737922db2b4bcc6f584c43c0a9853a6349c7291f97e`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a01096bfa0ab40a33a9409a21d6c1c0f20bcb9b6412e08cdcd371efb0b93b`  
		Last Modified: Mon, 09 Sep 2024 23:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9419c76ef9247e2a49e05fa427e6e19f2dc144b369d76fb96be3f36850610`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 7.0 MB (6984291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563c76e12f59745be55682bd551dd50cd984cd163c7b40974f19d0c2846bcf9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 88.4 KB (88391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ad67ac7fc1eecda198145aa433ca588a7633bd7d681b261686a26d8107ac9`  
		Last Modified: Mon, 09 Sep 2024 23:53:44 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c841feeb1b32629acc8ca755a64e8b62e00c6ae4215cd2e910cae7f7738b9`  
		Last Modified: Mon, 09 Sep 2024 23:53:46 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b0e71d339a3ab7b10a136d9c9e395b9c2c783a4d4e5b73f2d71aafeb6ac52`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375726cb9e08ae9527f0185b475e26e364bd6260d8cd24f71cd371e8c6a286dc`  
		Last Modified: Mon, 09 Sep 2024 23:53:45 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:c447c43d3b5bc7749ff3496a06b93b2ab807863d65981f7a78bfce39ed657bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266cda8cd92592207c4c6a6921c207d6782cae235c99819115cf799c9ffeb18e`

```dockerfile
```

-	Layers:
	-	`sha256:f97aa4568ee7321081089959eb269de2da430042ee94ef28d05b3bad3331ffd6`  
		Last Modified: Mon, 09 Sep 2024 23:53:43 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:7792b13addc6ed6a861a7072a423b670420225435d3ce343bd040c891c278636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121147450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0086daff2a557d25daff22a00c4dd8ff328d8f9be542d20e1e8079857388822`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ceed9dcf1fa64d9d597d87991fe2cf573abcdbc71234d48c56934567a0404c`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 16.6 MB (16570446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4f5814a89cb47d5589422329f364480c7f48d77be4e8cd1b8e76bf4f08ce7`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 17.1 MB (17103038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a9997cd15e7365c0b536f26f24b675dc87fb702dac2fd7dc49bc135bf3fea`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 17.8 MB (17771129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309171621269d9bb639255e1d0271bba63d925d3acc913597b8d9375613cadd`  
		Last Modified: Sat, 07 Sep 2024 02:22:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075d49c03c21a287246a41baf7810ed2a633c4559904a18684fdf9d9a47bc5a`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f94772be826fddb813f56152eca2eb28ad9ad36af3396a29893d16edb2458`  
		Last Modified: Sat, 07 Sep 2024 02:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c6cec47bdc84ac033aadebeb4278876d3815deb33b86b88fe4db4a756316f`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 6.3 MB (6308146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970185c8f0f65dc61cb7cede5f8398df93a6b4a1d01ec11bf1986d5889cb5b9e`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 84.5 KB (84486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5114dc189d3c23463831fa6fd843435d2272f2ce94b6d3cbcda85fd7c2cdb`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2232ccbfee55d492c7c0158bb5bd9bfcb0b69db3ebe2d61cb18af0a5f9fac67f`  
		Last Modified: Sat, 07 Sep 2024 13:21:33 GMT  
		Size: 53.1 MB (53062898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa12b57340218957a1a92ce8bb0d3704c7d78dfca411cd06e7f96213af3e89`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066bc852ed10399fc3fbd3ae0e8a5a56bf2ecf27e5cdf05aff0f948c4e20276b`  
		Last Modified: Sat, 07 Sep 2024 13:21:32 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:84adb8e5f65e3226756cd46faf02c7e67f88b94da37b5a9e6c9ebe4ea7ebdeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246b8ab470241ff0a3196b9c199889037c7926685ae82565948df5267df99ffe`

```dockerfile
```

-	Layers:
	-	`sha256:a61a8daec7fe32c2d9aa5f93e31013e0fac92809dd42e7a154d627d3f4335374`  
		Last Modified: Sat, 07 Sep 2024 13:21:31 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7600dc8fc3557d7ee7a19921a4d8fbe28f56aed480a936dfd9d51592560a330f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122837107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9d41861c64112cb8a31a202d69e0803e0adbd65012ac57b637f37645cbec8f`
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:fa9679aabf00703df98795b58f57ee39d82df6fba557562917bdd079c67fc20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db00fd33884626a893016c32ade9c6023eec620dd2a748e706ed90e7f2a493d7`

```dockerfile
```

-	Layers:
	-	`sha256:a1a57225559aee5e90d2a51207bf08c81342d2ee35e16337e1e4825b4bf37d96`  
		Last Modified: Sat, 07 Sep 2024 12:27:45 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:a37cf925e3846f27b2cd3d336e1fe334c220a2b68eed163466dcf69937559248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:4c8eef37a0c86aa06ad5976c38a052ab7341a1da0d2a517ff066c597e1a2102c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200017471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e9353bddaa42357f13d48483a35ce21c79258551e834702023e0be650aa46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:02:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:02:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332592d922e5dded83a183a722216fbf8d9e16270fa585874df3af5575477ec`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93745372d1a79c87a62454b598858a6f6cc1df8d2be9447cb3d204391ed7d0`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 361.5 KB (361489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6601eeb9638e45c268f11b45669f33c9878b81e18a865f16bc7fd97e985e4ee2`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf3732134bbe550cc9c2e1b8b2c61d7936c1c67a4e30c2cd946c7b085f7460`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679fc02a704b5f3823dc3c6ce6c94090c3b6f3393d34a45c20923b882d691fe`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 18.9 MB (18927866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca67afd286db97657f82fb6017b463e91c31a9b6c95ca07303a34b1d67aef2`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0db3426e28bff54c66b4018a4d03f6f239a2d8ea5308f11a30a59f9b1da54`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfae033be6705adac5640f96e61ba34c52452d7cc66d3db3685bbf1f1578c12`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ed372f37d2e0280f8a8c5f2f6183bf3075554a845fe9e22cb302897ae17f`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 19.3 MB (19257059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3aec99b5a36f7be293d446c07dce9436a71d75b98e743b257a76f3f64c11fa`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5167e8fbb6489585b5ca239706c1c8c7bd7bdf7728fe44e4937491dbb07b6324`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8274b4c972ec015a52de9b8db479c9826c7056fe4ff1173b7be79cca237aea`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfce3c544d708f6342c748468289910bc3f1d4f3e8caf473a55b0d7b0df3dec`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 19.7 MB (19694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:498644c5c8316f5838bb0230478d1d6a6a2d605565f77cee2ce21c0397ba2ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:d81f5c1b9b9d56091531cbb3182601456326326604ff5642423fd919e8979931
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303653669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7695755b060cf4ec5e764139fb8a58ddc668e4466af66b9a20922148cb39aca5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 23:01:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:34 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:03:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:03:03 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:03:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:03:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:03:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:03:29 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:03:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c29f54c38c8b02c86498d73c31eb3d36f358aaafa25a67bdaddbb9a815990`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b603e2073aa84109fb98a1b088d08dd96542021ca7b8d9a1d30d785ff07df3`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 508.7 KB (508711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b50df88404825ac89453a528e1ef8a629d3dfa73a399c952ab01fe9e1abde`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fc164dee199fccb9b7fc7356ef9996d4f35121a3dce65703b4a2df5d7d20e`  
		Last Modified: Mon, 09 Sep 2024 23:03:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de839b5793abb845839d438ae5a02bf0a4bff732f95d0655c974d23f8e25901`  
		Last Modified: Mon, 09 Sep 2024 23:04:00 GMT  
		Size: 18.9 MB (18948885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b580a2f4eafc12d5502ac12d93b3aa30042f06afec6693322be9951059997`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8769a644370e1c94ab17e594933aa1e88310dd53fd1302eec415650838d1700`  
		Last Modified: Mon, 09 Sep 2024 23:03:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aafd716e09f3d540616c96a94e5ffcfd86268eca243843dc3b6f2267863b91`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596392f006d8526cf7bceb0fa52b2dc3af98d886887dabff6de92e38e138261`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.3 MB (19274080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9ee955fe7803d110b91135ae86b7c85989afb8de8b6ecefc9baaa2a4f5ee4`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b3fb83746447614f7710e439d1176cbf295603cc3959f508d60dabbab0a16`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5436fa40a0efad7b0ba801aa9914421647ceb9836ea315c023c4c9dc6969e`  
		Last Modified: Mon, 09 Sep 2024 23:03:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d0ffac27e5f65775fec5b2f4c2237f46a88e46c24ab0f42fccf1876993fa89`  
		Last Modified: Mon, 09 Sep 2024 23:03:57 GMT  
		Size: 19.7 MB (19707065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:25fb7b70c8a560f15efbcfd426732a250aa1f0958ca12d86028d74bfb37cd608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:4c8eef37a0c86aa06ad5976c38a052ab7341a1da0d2a517ff066c597e1a2102c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200017471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e9353bddaa42357f13d48483a35ce21c79258551e834702023e0be650aa46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 23:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 23:02:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Mon, 09 Sep 2024 23:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 09 Sep 2024 23:02:22 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 09 Sep 2024 23:02:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Sep 2024 23:02:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 23:02:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 09 Sep 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 09 Sep 2024 23:02:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332592d922e5dded83a183a722216fbf8d9e16270fa585874df3af5575477ec`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da93745372d1a79c87a62454b598858a6f6cc1df8d2be9447cb3d204391ed7d0`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 361.5 KB (361489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6601eeb9638e45c268f11b45669f33c9878b81e18a865f16bc7fd97e985e4ee2`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf3732134bbe550cc9c2e1b8b2c61d7936c1c67a4e30c2cd946c7b085f7460`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679fc02a704b5f3823dc3c6ce6c94090c3b6f3393d34a45c20923b882d691fe`  
		Last Modified: Mon, 09 Sep 2024 23:02:48 GMT  
		Size: 18.9 MB (18927866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca67afd286db97657f82fb6017b463e91c31a9b6c95ca07303a34b1d67aef2`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0db3426e28bff54c66b4018a4d03f6f239a2d8ea5308f11a30a59f9b1da54`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfae033be6705adac5640f96e61ba34c52452d7cc66d3db3685bbf1f1578c12`  
		Last Modified: Mon, 09 Sep 2024 23:02:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ed372f37d2e0280f8a8c5f2f6183bf3075554a845fe9e22cb302897ae17f`  
		Last Modified: Mon, 09 Sep 2024 23:02:46 GMT  
		Size: 19.3 MB (19257059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3aec99b5a36f7be293d446c07dce9436a71d75b98e743b257a76f3f64c11fa`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5167e8fbb6489585b5ca239706c1c8c7bd7bdf7728fe44e4937491dbb07b6324`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8274b4c972ec015a52de9b8db479c9826c7056fe4ff1173b7be79cca237aea`  
		Last Modified: Mon, 09 Sep 2024 23:02:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfce3c544d708f6342c748468289910bc3f1d4f3e8caf473a55b0d7b0df3dec`  
		Last Modified: Mon, 09 Sep 2024 23:02:47 GMT  
		Size: 19.7 MB (19694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
