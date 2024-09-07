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
-	[`docker:27.2.0`](#docker2720)
-	[`docker:27.2.0-alpine3.20`](#docker2720-alpine320)
-	[`docker:27.2.0-cli`](#docker2720-cli)
-	[`docker:27.2.0-cli-alpine3.20`](#docker2720-cli-alpine320)
-	[`docker:27.2.0-dind`](#docker2720-dind)
-	[`docker:27.2.0-dind-alpine3.20`](#docker2720-dind-alpine320)
-	[`docker:27.2.0-dind-rootless`](#docker2720-dind-rootless)
-	[`docker:27.2.0-windowsservercore`](#docker2720-windowsservercore)
-	[`docker:27.2.0-windowsservercore-1809`](#docker2720-windowsservercore-1809)
-	[`docker:27.2.0-windowsservercore-ltsc2022`](#docker2720-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
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
$ docker pull docker@sha256:b0d5aafe0208821bdbe683e141cac9dac1a4ff30e5f56c7ae1359cbbeeb1d43f
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
$ docker pull docker@sha256:6ecc4797d7fd165cb322ff2249817633dc1f0063493eaaae51b060e96f817639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67051181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d1a0a6eeffb46012358ee49be7207e1ad437196afc818a45d84a616e40f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:949833a7d3a6cf9830ea4dbcc450cfacbb0f968be68136ddb32d8185ca036318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765f2662d20b39ba3767e01a47666f092782b3704d1a0304fc1fbdebd08c57e5`

```dockerfile
```

-	Layers:
	-	`sha256:dd1eb0c2b9a1555ad2485fbaa1ee07512f694cfcb2df8dbc423a401a28d390d1`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:c358f3000b736a52dc1f5a6b5d38518d2d6dda817387096b925e61a0afce790a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62652673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04cb20b033eab2a1983d82c604ef6f9df0cc6e46b3e173df99cb5d1dd93fbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1926340345cfb0a7fe0ca0148b3e2e777781fefd99d6e747a3ecabf09ae3b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2a015819fd49c55db699b1a53efbbff73791fda9af7b14673ae3beb27fb50`

```dockerfile
```

-	Layers:
	-	`sha256:b4c1e47ed34c8d63a0aa353603824dc724b91b653deb4e926480c68c2718cfc9`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:90c3c35405f87d1995cd49f58f83aee5abec2d1c77dfdb71d171a8f6607e6d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61686124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727dcb0bc39c215426cb5ef8788e2988bafc6e6262dbb79674937465503c3333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a088502335df7562d09f9b2946827c1d66e655c0f05a52366dc651cd2f034711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f812bd756a4d09a43a8e9b5c02e8d6da59f1ba47a7f934adce0b71b2b8b6226`

```dockerfile
```

-	Layers:
	-	`sha256:c5b452f46f632ee1ce872f6357d8beea2ca96d34059d4cdc1144cd8daaad654f`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 38.1 KB (38071 bytes)  
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
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
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
$ docker pull docker@sha256:d387e5f5f938c28b52664293ba33f3c4b66a2ff4b7f0b74c5d05bdd94cafefba
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
$ docker pull docker@sha256:e3fbe21c151e4271d73fa228238bc61f32f660c550aa54e3527a460c27bac3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146696891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9187071f9b3d29959b0bf9a17b644db2d13e09317b504659a69884c6717ac1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7ebf14e366b1f6bb3a236c7afda2fa7f972ec82687bdfb1faa44ff909b3c7`  
		Last Modified: Wed, 28 Aug 2024 20:55:20 GMT  
		Size: 8.0 MB (7981883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70774fd8129e715db6bdde0a5fa9a8126035d57497c7abbf3918ff783e3839b9`  
		Last Modified: Wed, 28 Aug 2024 20:55:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75bde5fae086c68bd31219b257fd17de34da8ae7534ba873f2893aecb170265`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 17.3 MB (17266013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d280a0d728e728847e4bf2aea17b91f3d0b0341f060af4931e99f3701dd251a3`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e7e06e5fa6595fc74a6b371d01d11c33d00755afee8c9e5526b26db04bdca`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee3d5382660f041e5d6a4e7e5eed70a981eb51d8f65e980dc17b77257f5d1d`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e7d5e3ae6089103a06ae9421106617e42616bccfb18af4a99a047a339b59cf`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6843b239ba63d521157d7d1a46d9346bf6fd58eec87be84f52f99b62a8fb2d47`  
		Last Modified: Wed, 28 Aug 2024 20:55:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c047d9d5cf44cdaa49f139b96bfad8456b4544e7f8dac65b22512b54b5c27785`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 7.0 MB (7034976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8566c5e148875679770fa70b5d8461643fe4f3e523cc4c23fd5048921979993`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 98.7 KB (98665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e81cd465f9ee02216b68ffcd601579cf2b466ec9cfe9eab7d1848715d5efb6`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfc280f1208cfd219d0f5c9ce8a5485366216b0690ca15eac47242a174ec3ec`  
		Last Modified: Wed, 28 Aug 2024 21:48:47 GMT  
		Size: 52.4 MB (52400296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f850c0ae6138cdad5371b2e2f80f46619b8f1e83fd23719f35d80c4e68fd4`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494ac230758233bbef46064dc8f7048fff0763039a7c97d01acd30d1e1a6b16`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61d4b5e595f4a9dcd2d5b73dd64893b48b8b5c325e6c2a77f7d87c3bf774b63`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.0 MB (1023147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970a08325e433d212e5137f22b0c5f9ea602fe6d34c30ff0af92e85d826d457`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f824c9ac49392520b799e62abf06ca24190d5c747d6a8665d62f17c60adaf174`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468a19c79fccedbe38a88979c4a5da92b1a73c727a9b3fc58e11bbabd3e9256`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 22.8 MB (22835883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49084cd44b920e2654ce7a8f2bace247f0acd7ddfc481e9365b9c39c01dfe57`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b7cefe17c5a87b42bf6cfcec3b08ade5272c29f153f8fbcb770707bc1c20ccb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6630734a56a43074699439ce4c6d79ac0ec2972110823e0d46a936ece911b64f`

```dockerfile
```

-	Layers:
	-	`sha256:c50ad41cecb6f30ac11d08ace289d54c454da27e48229ef60c118eee48306b88`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:07546d30ede0a05226bf16bd88fc0a63c9facc86586728958b4c80192695068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:0609f36687bf0504b97ad2081e11e72b32ddeeaa13cec6b048e3203430ef3089
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199734114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e1d842fb99c5efb58e541674f93c74cd42646f4b55c3b595d31040d55bc8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 20:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:55:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:55:45 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:55:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:55:56 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:55:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:55:58 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:56:09 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:56:17 GMT
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
	-	`sha256:4cf2d920f1909f2588f1ff04da758a04650a2c83aa8846cdd27b355d5a3a977f`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d5e4634044af44742fd5ffcf53035c01b840441d1a6cbef4ac7c746079486`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 360.5 KB (360496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d90ca9a81e4b14450116f867b3fb9c986db7e6175327f0b8504e381923861`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e248f39ea321d362cd75a8d419e0ea56ae669b863c01760c1c8e4b3dddb81`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963453be438ca99012a6b206cb013b6e169d667b571731db178d8bb33f606b96`  
		Last Modified: Wed, 28 Aug 2024 20:56:27 GMT  
		Size: 18.6 MB (18648166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d3ae2221337464147d8ca5bf07cba7df651cea8324b58d3627e3dcfeb949c`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf2a088e2ea59c0a94284511a62711915af818e15bd695a7a25fd6624e26d2`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088754d192ca79a523ab3c6fdb3cecf0d5400910e48a70be1bc99b09c4d545`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ae88bbccf2cdc37064a22b1efaeec5ce004676d3da7f6fe9568b4421daa89`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.3 MB (19256026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30b29b13ead92894d4f6fb2e79593d75d134dfdd002ef8b65a4e79c03408b3c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039c01e50286e2d55794b477a1c9be4a1865ddc62c5d442e8d1ce8bf23ba99c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57d9a6f993df099347c867bae5736a2f45b5c6a82fac6d770c981623610e6c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08adb1197ed079a2603242de73317d9b6741e36aef8c5ca31089a2af9891fbf0`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.7 MB (19692868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:f79c41f6313d87137a86a10b6766aa1a8d7fd7222566fc535e8b035ba5275d30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303408245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadc037faf2c53d92a835b8acd557af08233054e3c014a15ee63fcd6bd6b372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 20:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:04 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:58:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:58:06 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:58:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:58:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:58:56 GMT
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
	-	`sha256:bea7b5749b0c9fb1ac4216c0ec3cc34e8c4be1bce91440d5e1af1649c9c44b28`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d3dbb1662bf2bd051db933d8f25a808f934a2193a77362aabad59b3ea4662`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 517.4 KB (517436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841d1c8c7a9173bff32240c17bdffdf38c681b5b4397203e950a003472b2905`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810d7ba2db013f2f7325865ca49bb77484db37c509e0be28424d521b6e2a2d7`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a162087fe10bf8028abdf75d0405a7ef811f88a987ab854203312c22eb9861`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 18.7 MB (18677122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56da2e9f3099c19aedac3881cfe6bfb105ef07c87df79d1b0f0bc45b58e650`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d7596bf7393641bb335dc26dfb31a26d85fc8df54fa9f954191d85af23e6a1`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd2f20acdd7b9e4ec1e66f6ad8e1339f99f84d83c63e45954a6fb65ff14dce`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16dde64c46ae532c4d1498a92b6e7b848d486b49c8f468ececc93c64f815bf`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.3 MB (19283380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c440d986f0bb5cd0d2b54b000f66d219d485fe01156c83e521ca043343eaa`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5e005da41696b2a54a882c54042a6f1d0b17d46c35764e13dc483553b2972`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b06d561699b752f24ba95b01207841e01d0719dfbe6a672e99ab376e6935c`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa9ddd1a61f5cb64f47bed02502a9aa201f815f7771313483742408303a65b`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.7 MB (19715375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:85054315edda96f30ed9f7567edc068176f539f4823dd4dc9f573f205c60cfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:f79c41f6313d87137a86a10b6766aa1a8d7fd7222566fc535e8b035ba5275d30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303408245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadc037faf2c53d92a835b8acd557af08233054e3c014a15ee63fcd6bd6b372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 20:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:04 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:58:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:58:06 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:58:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:58:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:58:56 GMT
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
	-	`sha256:bea7b5749b0c9fb1ac4216c0ec3cc34e8c4be1bce91440d5e1af1649c9c44b28`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d3dbb1662bf2bd051db933d8f25a808f934a2193a77362aabad59b3ea4662`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 517.4 KB (517436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841d1c8c7a9173bff32240c17bdffdf38c681b5b4397203e950a003472b2905`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810d7ba2db013f2f7325865ca49bb77484db37c509e0be28424d521b6e2a2d7`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a162087fe10bf8028abdf75d0405a7ef811f88a987ab854203312c22eb9861`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 18.7 MB (18677122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56da2e9f3099c19aedac3881cfe6bfb105ef07c87df79d1b0f0bc45b58e650`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d7596bf7393641bb335dc26dfb31a26d85fc8df54fa9f954191d85af23e6a1`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd2f20acdd7b9e4ec1e66f6ad8e1339f99f84d83c63e45954a6fb65ff14dce`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16dde64c46ae532c4d1498a92b6e7b848d486b49c8f468ececc93c64f815bf`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.3 MB (19283380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c440d986f0bb5cd0d2b54b000f66d219d485fe01156c83e521ca043343eaa`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5e005da41696b2a54a882c54042a6f1d0b17d46c35764e13dc483553b2972`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b06d561699b752f24ba95b01207841e01d0719dfbe6a672e99ab376e6935c`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa9ddd1a61f5cb64f47bed02502a9aa201f815f7771313483742408303a65b`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.7 MB (19715375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:5eebe2261795454a6c9a54eed64f81f6ebd7b007ec70efd6bf3fffd090ec4843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:0609f36687bf0504b97ad2081e11e72b32ddeeaa13cec6b048e3203430ef3089
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199734114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e1d842fb99c5efb58e541674f93c74cd42646f4b55c3b595d31040d55bc8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 20:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:55:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:55:45 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:55:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:55:56 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:55:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:55:58 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:56:09 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:56:17 GMT
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
	-	`sha256:4cf2d920f1909f2588f1ff04da758a04650a2c83aa8846cdd27b355d5a3a977f`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d5e4634044af44742fd5ffcf53035c01b840441d1a6cbef4ac7c746079486`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 360.5 KB (360496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d90ca9a81e4b14450116f867b3fb9c986db7e6175327f0b8504e381923861`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e248f39ea321d362cd75a8d419e0ea56ae669b863c01760c1c8e4b3dddb81`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963453be438ca99012a6b206cb013b6e169d667b571731db178d8bb33f606b96`  
		Last Modified: Wed, 28 Aug 2024 20:56:27 GMT  
		Size: 18.6 MB (18648166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d3ae2221337464147d8ca5bf07cba7df651cea8324b58d3627e3dcfeb949c`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf2a088e2ea59c0a94284511a62711915af818e15bd695a7a25fd6624e26d2`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088754d192ca79a523ab3c6fdb3cecf0d5400910e48a70be1bc99b09c4d545`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ae88bbccf2cdc37064a22b1efaeec5ce004676d3da7f6fe9568b4421daa89`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.3 MB (19256026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30b29b13ead92894d4f6fb2e79593d75d134dfdd002ef8b65a4e79c03408b3c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039c01e50286e2d55794b477a1c9be4a1865ddc62c5d442e8d1ce8bf23ba99c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57d9a6f993df099347c867bae5736a2f45b5c6a82fac6d770c981623610e6c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08adb1197ed079a2603242de73317d9b6741e36aef8c5ca31089a2af9891fbf0`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.7 MB (19692868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2`

```console
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
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
$ docker pull docker@sha256:b0d5aafe0208821bdbe683e141cac9dac1a4ff30e5f56c7ae1359cbbeeb1d43f
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
$ docker pull docker@sha256:6ecc4797d7fd165cb322ff2249817633dc1f0063493eaaae51b060e96f817639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67051181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d1a0a6eeffb46012358ee49be7207e1ad437196afc818a45d84a616e40f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:949833a7d3a6cf9830ea4dbcc450cfacbb0f968be68136ddb32d8185ca036318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765f2662d20b39ba3767e01a47666f092782b3704d1a0304fc1fbdebd08c57e5`

```dockerfile
```

-	Layers:
	-	`sha256:dd1eb0c2b9a1555ad2485fbaa1ee07512f694cfcb2df8dbc423a401a28d390d1`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:c358f3000b736a52dc1f5a6b5d38518d2d6dda817387096b925e61a0afce790a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62652673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04cb20b033eab2a1983d82c604ef6f9df0cc6e46b3e173df99cb5d1dd93fbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1926340345cfb0a7fe0ca0148b3e2e777781fefd99d6e747a3ecabf09ae3b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2a015819fd49c55db699b1a53efbbff73791fda9af7b14673ae3beb27fb50`

```dockerfile
```

-	Layers:
	-	`sha256:b4c1e47ed34c8d63a0aa353603824dc724b91b653deb4e926480c68c2718cfc9`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:90c3c35405f87d1995cd49f58f83aee5abec2d1c77dfdb71d171a8f6607e6d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61686124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727dcb0bc39c215426cb5ef8788e2988bafc6e6262dbb79674937465503c3333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a088502335df7562d09f9b2946827c1d66e655c0f05a52366dc651cd2f034711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f812bd756a4d09a43a8e9b5c02e8d6da59f1ba47a7f934adce0b71b2b8b6226`

```dockerfile
```

-	Layers:
	-	`sha256:c5b452f46f632ee1ce872f6357d8beea2ca96d34059d4cdc1144cd8daaad654f`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 38.1 KB (38071 bytes)  
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
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
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
$ docker pull docker@sha256:d387e5f5f938c28b52664293ba33f3c4b66a2ff4b7f0b74c5d05bdd94cafefba
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
$ docker pull docker@sha256:e3fbe21c151e4271d73fa228238bc61f32f660c550aa54e3527a460c27bac3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146696891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9187071f9b3d29959b0bf9a17b644db2d13e09317b504659a69884c6717ac1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7ebf14e366b1f6bb3a236c7afda2fa7f972ec82687bdfb1faa44ff909b3c7`  
		Last Modified: Wed, 28 Aug 2024 20:55:20 GMT  
		Size: 8.0 MB (7981883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70774fd8129e715db6bdde0a5fa9a8126035d57497c7abbf3918ff783e3839b9`  
		Last Modified: Wed, 28 Aug 2024 20:55:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75bde5fae086c68bd31219b257fd17de34da8ae7534ba873f2893aecb170265`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 17.3 MB (17266013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d280a0d728e728847e4bf2aea17b91f3d0b0341f060af4931e99f3701dd251a3`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e7e06e5fa6595fc74a6b371d01d11c33d00755afee8c9e5526b26db04bdca`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee3d5382660f041e5d6a4e7e5eed70a981eb51d8f65e980dc17b77257f5d1d`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e7d5e3ae6089103a06ae9421106617e42616bccfb18af4a99a047a339b59cf`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6843b239ba63d521157d7d1a46d9346bf6fd58eec87be84f52f99b62a8fb2d47`  
		Last Modified: Wed, 28 Aug 2024 20:55:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c047d9d5cf44cdaa49f139b96bfad8456b4544e7f8dac65b22512b54b5c27785`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 7.0 MB (7034976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8566c5e148875679770fa70b5d8461643fe4f3e523cc4c23fd5048921979993`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 98.7 KB (98665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e81cd465f9ee02216b68ffcd601579cf2b466ec9cfe9eab7d1848715d5efb6`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfc280f1208cfd219d0f5c9ce8a5485366216b0690ca15eac47242a174ec3ec`  
		Last Modified: Wed, 28 Aug 2024 21:48:47 GMT  
		Size: 52.4 MB (52400296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f850c0ae6138cdad5371b2e2f80f46619b8f1e83fd23719f35d80c4e68fd4`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494ac230758233bbef46064dc8f7048fff0763039a7c97d01acd30d1e1a6b16`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61d4b5e595f4a9dcd2d5b73dd64893b48b8b5c325e6c2a77f7d87c3bf774b63`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.0 MB (1023147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970a08325e433d212e5137f22b0c5f9ea602fe6d34c30ff0af92e85d826d457`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f824c9ac49392520b799e62abf06ca24190d5c747d6a8665d62f17c60adaf174`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468a19c79fccedbe38a88979c4a5da92b1a73c727a9b3fc58e11bbabd3e9256`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 22.8 MB (22835883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49084cd44b920e2654ce7a8f2bace247f0acd7ddfc481e9365b9c39c01dfe57`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b7cefe17c5a87b42bf6cfcec3b08ade5272c29f153f8fbcb770707bc1c20ccb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6630734a56a43074699439ce4c6d79ac0ec2972110823e0d46a936ece911b64f`

```dockerfile
```

-	Layers:
	-	`sha256:c50ad41cecb6f30ac11d08ace289d54c454da27e48229ef60c118eee48306b88`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2-windowsservercore`

```console
$ docker pull docker@sha256:07546d30ede0a05226bf16bd88fc0a63c9facc86586728958b4c80192695068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27.2-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:0609f36687bf0504b97ad2081e11e72b32ddeeaa13cec6b048e3203430ef3089
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199734114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e1d842fb99c5efb58e541674f93c74cd42646f4b55c3b595d31040d55bc8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 20:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:55:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:55:45 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:55:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:55:56 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:55:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:55:58 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:56:09 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:56:17 GMT
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
	-	`sha256:4cf2d920f1909f2588f1ff04da758a04650a2c83aa8846cdd27b355d5a3a977f`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d5e4634044af44742fd5ffcf53035c01b840441d1a6cbef4ac7c746079486`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 360.5 KB (360496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d90ca9a81e4b14450116f867b3fb9c986db7e6175327f0b8504e381923861`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e248f39ea321d362cd75a8d419e0ea56ae669b863c01760c1c8e4b3dddb81`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963453be438ca99012a6b206cb013b6e169d667b571731db178d8bb33f606b96`  
		Last Modified: Wed, 28 Aug 2024 20:56:27 GMT  
		Size: 18.6 MB (18648166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d3ae2221337464147d8ca5bf07cba7df651cea8324b58d3627e3dcfeb949c`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf2a088e2ea59c0a94284511a62711915af818e15bd695a7a25fd6624e26d2`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088754d192ca79a523ab3c6fdb3cecf0d5400910e48a70be1bc99b09c4d545`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ae88bbccf2cdc37064a22b1efaeec5ce004676d3da7f6fe9568b4421daa89`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.3 MB (19256026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30b29b13ead92894d4f6fb2e79593d75d134dfdd002ef8b65a4e79c03408b3c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039c01e50286e2d55794b477a1c9be4a1865ddc62c5d442e8d1ce8bf23ba99c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57d9a6f993df099347c867bae5736a2f45b5c6a82fac6d770c981623610e6c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08adb1197ed079a2603242de73317d9b6741e36aef8c5ca31089a2af9891fbf0`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.7 MB (19692868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.2-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:f79c41f6313d87137a86a10b6766aa1a8d7fd7222566fc535e8b035ba5275d30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303408245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadc037faf2c53d92a835b8acd557af08233054e3c014a15ee63fcd6bd6b372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 20:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:04 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:58:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:58:06 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:58:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:58:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:58:56 GMT
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
	-	`sha256:bea7b5749b0c9fb1ac4216c0ec3cc34e8c4be1bce91440d5e1af1649c9c44b28`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d3dbb1662bf2bd051db933d8f25a808f934a2193a77362aabad59b3ea4662`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 517.4 KB (517436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841d1c8c7a9173bff32240c17bdffdf38c681b5b4397203e950a003472b2905`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810d7ba2db013f2f7325865ca49bb77484db37c509e0be28424d521b6e2a2d7`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a162087fe10bf8028abdf75d0405a7ef811f88a987ab854203312c22eb9861`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 18.7 MB (18677122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56da2e9f3099c19aedac3881cfe6bfb105ef07c87df79d1b0f0bc45b58e650`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d7596bf7393641bb335dc26dfb31a26d85fc8df54fa9f954191d85af23e6a1`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd2f20acdd7b9e4ec1e66f6ad8e1339f99f84d83c63e45954a6fb65ff14dce`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16dde64c46ae532c4d1498a92b6e7b848d486b49c8f468ececc93c64f815bf`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.3 MB (19283380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c440d986f0bb5cd0d2b54b000f66d219d485fe01156c83e521ca043343eaa`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5e005da41696b2a54a882c54042a6f1d0b17d46c35764e13dc483553b2972`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b06d561699b752f24ba95b01207841e01d0719dfbe6a672e99ab376e6935c`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa9ddd1a61f5cb64f47bed02502a9aa201f815f7771313483742408303a65b`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.7 MB (19715375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2-windowsservercore-1809`

```console
$ docker pull docker@sha256:85054315edda96f30ed9f7567edc068176f539f4823dd4dc9f573f205c60cfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27.2-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:f79c41f6313d87137a86a10b6766aa1a8d7fd7222566fc535e8b035ba5275d30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303408245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadc037faf2c53d92a835b8acd557af08233054e3c014a15ee63fcd6bd6b372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 20:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:04 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:58:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:58:06 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:58:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:58:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:58:56 GMT
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
	-	`sha256:bea7b5749b0c9fb1ac4216c0ec3cc34e8c4be1bce91440d5e1af1649c9c44b28`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d3dbb1662bf2bd051db933d8f25a808f934a2193a77362aabad59b3ea4662`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 517.4 KB (517436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841d1c8c7a9173bff32240c17bdffdf38c681b5b4397203e950a003472b2905`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810d7ba2db013f2f7325865ca49bb77484db37c509e0be28424d521b6e2a2d7`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a162087fe10bf8028abdf75d0405a7ef811f88a987ab854203312c22eb9861`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 18.7 MB (18677122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56da2e9f3099c19aedac3881cfe6bfb105ef07c87df79d1b0f0bc45b58e650`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d7596bf7393641bb335dc26dfb31a26d85fc8df54fa9f954191d85af23e6a1`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd2f20acdd7b9e4ec1e66f6ad8e1339f99f84d83c63e45954a6fb65ff14dce`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16dde64c46ae532c4d1498a92b6e7b848d486b49c8f468ececc93c64f815bf`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.3 MB (19283380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c440d986f0bb5cd0d2b54b000f66d219d485fe01156c83e521ca043343eaa`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5e005da41696b2a54a882c54042a6f1d0b17d46c35764e13dc483553b2972`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b06d561699b752f24ba95b01207841e01d0719dfbe6a672e99ab376e6935c`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa9ddd1a61f5cb64f47bed02502a9aa201f815f7771313483742408303a65b`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.7 MB (19715375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:5eebe2261795454a6c9a54eed64f81f6ebd7b007ec70efd6bf3fffd090ec4843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27.2-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:0609f36687bf0504b97ad2081e11e72b32ddeeaa13cec6b048e3203430ef3089
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199734114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e1d842fb99c5efb58e541674f93c74cd42646f4b55c3b595d31040d55bc8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 20:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:55:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:55:45 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:55:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:55:56 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:55:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:55:58 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:56:09 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:56:17 GMT
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
	-	`sha256:4cf2d920f1909f2588f1ff04da758a04650a2c83aa8846cdd27b355d5a3a977f`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d5e4634044af44742fd5ffcf53035c01b840441d1a6cbef4ac7c746079486`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 360.5 KB (360496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d90ca9a81e4b14450116f867b3fb9c986db7e6175327f0b8504e381923861`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e248f39ea321d362cd75a8d419e0ea56ae669b863c01760c1c8e4b3dddb81`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963453be438ca99012a6b206cb013b6e169d667b571731db178d8bb33f606b96`  
		Last Modified: Wed, 28 Aug 2024 20:56:27 GMT  
		Size: 18.6 MB (18648166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d3ae2221337464147d8ca5bf07cba7df651cea8324b58d3627e3dcfeb949c`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf2a088e2ea59c0a94284511a62711915af818e15bd695a7a25fd6624e26d2`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088754d192ca79a523ab3c6fdb3cecf0d5400910e48a70be1bc99b09c4d545`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ae88bbccf2cdc37064a22b1efaeec5ce004676d3da7f6fe9568b4421daa89`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.3 MB (19256026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30b29b13ead92894d4f6fb2e79593d75d134dfdd002ef8b65a4e79c03408b3c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039c01e50286e2d55794b477a1c9be4a1865ddc62c5d442e8d1ce8bf23ba99c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57d9a6f993df099347c867bae5736a2f45b5c6a82fac6d770c981623610e6c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08adb1197ed079a2603242de73317d9b6741e36aef8c5ca31089a2af9891fbf0`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.7 MB (19692868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.0`

```console
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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

### `docker:27.2.0` - linux; amd64

```console
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:27.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0` - linux; arm variant v7

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

### `docker:27.2.0` - unknown; unknown

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

### `docker:27.2.0` - linux; arm64 variant v8

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

### `docker:27.2.0` - unknown; unknown

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

## `docker:27.2.0-alpine3.20`

```console
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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

### `docker:27.2.0-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:27.2.0-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.0-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-alpine3.20` - linux; arm variant v7

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

### `docker:27.2.0-alpine3.20` - unknown; unknown

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

### `docker:27.2.0-alpine3.20` - linux; arm64 variant v8

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

### `docker:27.2.0-alpine3.20` - unknown; unknown

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

## `docker:27.2.0-cli`

```console
$ docker pull docker@sha256:b0d5aafe0208821bdbe683e141cac9dac1a4ff30e5f56c7ae1359cbbeeb1d43f
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

### `docker:27.2.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:6ecc4797d7fd165cb322ff2249817633dc1f0063493eaaae51b060e96f817639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67051181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d1a0a6eeffb46012358ee49be7207e1ad437196afc818a45d84a616e40f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:949833a7d3a6cf9830ea4dbcc450cfacbb0f968be68136ddb32d8185ca036318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765f2662d20b39ba3767e01a47666f092782b3704d1a0304fc1fbdebd08c57e5`

```dockerfile
```

-	Layers:
	-	`sha256:dd1eb0c2b9a1555ad2485fbaa1ee07512f694cfcb2df8dbc423a401a28d390d1`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:c358f3000b736a52dc1f5a6b5d38518d2d6dda817387096b925e61a0afce790a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62652673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04cb20b033eab2a1983d82c604ef6f9df0cc6e46b3e173df99cb5d1dd93fbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1926340345cfb0a7fe0ca0148b3e2e777781fefd99d6e747a3ecabf09ae3b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2a015819fd49c55db699b1a53efbbff73791fda9af7b14673ae3beb27fb50`

```dockerfile
```

-	Layers:
	-	`sha256:b4c1e47ed34c8d63a0aa353603824dc724b91b653deb4e926480c68c2718cfc9`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:90c3c35405f87d1995cd49f58f83aee5abec2d1c77dfdb71d171a8f6607e6d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61686124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727dcb0bc39c215426cb5ef8788e2988bafc6e6262dbb79674937465503c3333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a088502335df7562d09f9b2946827c1d66e655c0f05a52366dc651cd2f034711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f812bd756a4d09a43a8e9b5c02e8d6da59f1ba47a7f934adce0b71b2b8b6226`

```dockerfile
```

-	Layers:
	-	`sha256:c5b452f46f632ee1ce872f6357d8beea2ca96d34059d4cdc1144cd8daaad654f`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-cli` - linux; arm64 variant v8

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

### `docker:27.2.0-cli` - unknown; unknown

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

## `docker:27.2.0-cli-alpine3.20`

```console
$ docker pull docker@sha256:b0d5aafe0208821bdbe683e141cac9dac1a4ff30e5f56c7ae1359cbbeeb1d43f
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

### `docker:27.2.0-cli-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:6ecc4797d7fd165cb322ff2249817633dc1f0063493eaaae51b060e96f817639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67051181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d1a0a6eeffb46012358ee49be7207e1ad437196afc818a45d84a616e40f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2.0-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:949833a7d3a6cf9830ea4dbcc450cfacbb0f968be68136ddb32d8185ca036318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765f2662d20b39ba3767e01a47666f092782b3704d1a0304fc1fbdebd08c57e5`

```dockerfile
```

-	Layers:
	-	`sha256:dd1eb0c2b9a1555ad2485fbaa1ee07512f694cfcb2df8dbc423a401a28d390d1`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:c358f3000b736a52dc1f5a6b5d38518d2d6dda817387096b925e61a0afce790a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62652673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04cb20b033eab2a1983d82c604ef6f9df0cc6e46b3e173df99cb5d1dd93fbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.0-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:1926340345cfb0a7fe0ca0148b3e2e777781fefd99d6e747a3ecabf09ae3b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2a015819fd49c55db699b1a53efbbff73791fda9af7b14673ae3beb27fb50`

```dockerfile
```

-	Layers:
	-	`sha256:b4c1e47ed34c8d63a0aa353603824dc724b91b653deb4e926480c68c2718cfc9`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:90c3c35405f87d1995cd49f58f83aee5abec2d1c77dfdb71d171a8f6607e6d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61686124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727dcb0bc39c215426cb5ef8788e2988bafc6e6262dbb79674937465503c3333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:27.2.0-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:a088502335df7562d09f9b2946827c1d66e655c0f05a52366dc651cd2f034711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f812bd756a4d09a43a8e9b5c02e8d6da59f1ba47a7f934adce0b71b2b8b6226`

```dockerfile
```

-	Layers:
	-	`sha256:c5b452f46f632ee1ce872f6357d8beea2ca96d34059d4cdc1144cd8daaad654f`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-cli-alpine3.20` - linux; arm64 variant v8

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

### `docker:27.2.0-cli-alpine3.20` - unknown; unknown

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

## `docker:27.2.0-dind`

```console
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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

### `docker:27.2.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:27.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-dind` - linux; arm variant v7

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

### `docker:27.2.0-dind` - unknown; unknown

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

### `docker:27.2.0-dind` - linux; arm64 variant v8

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

### `docker:27.2.0-dind` - unknown; unknown

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

## `docker:27.2.0-dind-alpine3.20`

```console
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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

### `docker:27.2.0-dind-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:27.2.0-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.0-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.0-dind-alpine3.20` - linux; arm variant v7

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

### `docker:27.2.0-dind-alpine3.20` - unknown; unknown

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

### `docker:27.2.0-dind-alpine3.20` - linux; arm64 variant v8

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

### `docker:27.2.0-dind-alpine3.20` - unknown; unknown

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

## `docker:27.2.0-dind-rootless`

```console
$ docker pull docker@sha256:d387e5f5f938c28b52664293ba33f3c4b66a2ff4b7f0b74c5d05bdd94cafefba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.2.0-dind-rootless` - linux; amd64

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

### `docker:27.2.0-dind-rootless` - unknown; unknown

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

### `docker:27.2.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e3fbe21c151e4271d73fa228238bc61f32f660c550aa54e3527a460c27bac3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146696891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9187071f9b3d29959b0bf9a17b644db2d13e09317b504659a69884c6717ac1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7ebf14e366b1f6bb3a236c7afda2fa7f972ec82687bdfb1faa44ff909b3c7`  
		Last Modified: Wed, 28 Aug 2024 20:55:20 GMT  
		Size: 8.0 MB (7981883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70774fd8129e715db6bdde0a5fa9a8126035d57497c7abbf3918ff783e3839b9`  
		Last Modified: Wed, 28 Aug 2024 20:55:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75bde5fae086c68bd31219b257fd17de34da8ae7534ba873f2893aecb170265`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 17.3 MB (17266013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d280a0d728e728847e4bf2aea17b91f3d0b0341f060af4931e99f3701dd251a3`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e7e06e5fa6595fc74a6b371d01d11c33d00755afee8c9e5526b26db04bdca`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee3d5382660f041e5d6a4e7e5eed70a981eb51d8f65e980dc17b77257f5d1d`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e7d5e3ae6089103a06ae9421106617e42616bccfb18af4a99a047a339b59cf`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6843b239ba63d521157d7d1a46d9346bf6fd58eec87be84f52f99b62a8fb2d47`  
		Last Modified: Wed, 28 Aug 2024 20:55:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c047d9d5cf44cdaa49f139b96bfad8456b4544e7f8dac65b22512b54b5c27785`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 7.0 MB (7034976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8566c5e148875679770fa70b5d8461643fe4f3e523cc4c23fd5048921979993`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 98.7 KB (98665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e81cd465f9ee02216b68ffcd601579cf2b466ec9cfe9eab7d1848715d5efb6`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfc280f1208cfd219d0f5c9ce8a5485366216b0690ca15eac47242a174ec3ec`  
		Last Modified: Wed, 28 Aug 2024 21:48:47 GMT  
		Size: 52.4 MB (52400296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f850c0ae6138cdad5371b2e2f80f46619b8f1e83fd23719f35d80c4e68fd4`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494ac230758233bbef46064dc8f7048fff0763039a7c97d01acd30d1e1a6b16`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61d4b5e595f4a9dcd2d5b73dd64893b48b8b5c325e6c2a77f7d87c3bf774b63`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.0 MB (1023147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970a08325e433d212e5137f22b0c5f9ea602fe6d34c30ff0af92e85d826d457`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f824c9ac49392520b799e62abf06ca24190d5c747d6a8665d62f17c60adaf174`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468a19c79fccedbe38a88979c4a5da92b1a73c727a9b3fc58e11bbabd3e9256`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 22.8 MB (22835883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49084cd44b920e2654ce7a8f2bace247f0acd7ddfc481e9365b9c39c01dfe57`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b7cefe17c5a87b42bf6cfcec3b08ade5272c29f153f8fbcb770707bc1c20ccb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6630734a56a43074699439ce4c6d79ac0ec2972110823e0d46a936ece911b64f`

```dockerfile
```

-	Layers:
	-	`sha256:c50ad41cecb6f30ac11d08ace289d54c454da27e48229ef60c118eee48306b88`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.0-windowsservercore`

```console
$ docker pull docker@sha256:07546d30ede0a05226bf16bd88fc0a63c9facc86586728958b4c80192695068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27.2.0-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:0609f36687bf0504b97ad2081e11e72b32ddeeaa13cec6b048e3203430ef3089
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199734114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e1d842fb99c5efb58e541674f93c74cd42646f4b55c3b595d31040d55bc8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 20:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:55:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:55:45 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:55:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:55:56 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:55:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:55:58 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:56:09 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:56:17 GMT
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
	-	`sha256:4cf2d920f1909f2588f1ff04da758a04650a2c83aa8846cdd27b355d5a3a977f`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d5e4634044af44742fd5ffcf53035c01b840441d1a6cbef4ac7c746079486`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 360.5 KB (360496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d90ca9a81e4b14450116f867b3fb9c986db7e6175327f0b8504e381923861`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e248f39ea321d362cd75a8d419e0ea56ae669b863c01760c1c8e4b3dddb81`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963453be438ca99012a6b206cb013b6e169d667b571731db178d8bb33f606b96`  
		Last Modified: Wed, 28 Aug 2024 20:56:27 GMT  
		Size: 18.6 MB (18648166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d3ae2221337464147d8ca5bf07cba7df651cea8324b58d3627e3dcfeb949c`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf2a088e2ea59c0a94284511a62711915af818e15bd695a7a25fd6624e26d2`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088754d192ca79a523ab3c6fdb3cecf0d5400910e48a70be1bc99b09c4d545`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ae88bbccf2cdc37064a22b1efaeec5ce004676d3da7f6fe9568b4421daa89`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.3 MB (19256026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30b29b13ead92894d4f6fb2e79593d75d134dfdd002ef8b65a4e79c03408b3c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039c01e50286e2d55794b477a1c9be4a1865ddc62c5d442e8d1ce8bf23ba99c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57d9a6f993df099347c867bae5736a2f45b5c6a82fac6d770c981623610e6c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08adb1197ed079a2603242de73317d9b6741e36aef8c5ca31089a2af9891fbf0`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.7 MB (19692868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.2.0-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:f79c41f6313d87137a86a10b6766aa1a8d7fd7222566fc535e8b035ba5275d30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303408245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadc037faf2c53d92a835b8acd557af08233054e3c014a15ee63fcd6bd6b372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 20:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:04 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:58:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:58:06 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:58:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:58:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:58:56 GMT
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
	-	`sha256:bea7b5749b0c9fb1ac4216c0ec3cc34e8c4be1bce91440d5e1af1649c9c44b28`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d3dbb1662bf2bd051db933d8f25a808f934a2193a77362aabad59b3ea4662`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 517.4 KB (517436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841d1c8c7a9173bff32240c17bdffdf38c681b5b4397203e950a003472b2905`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810d7ba2db013f2f7325865ca49bb77484db37c509e0be28424d521b6e2a2d7`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a162087fe10bf8028abdf75d0405a7ef811f88a987ab854203312c22eb9861`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 18.7 MB (18677122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56da2e9f3099c19aedac3881cfe6bfb105ef07c87df79d1b0f0bc45b58e650`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d7596bf7393641bb335dc26dfb31a26d85fc8df54fa9f954191d85af23e6a1`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd2f20acdd7b9e4ec1e66f6ad8e1339f99f84d83c63e45954a6fb65ff14dce`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16dde64c46ae532c4d1498a92b6e7b848d486b49c8f468ececc93c64f815bf`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.3 MB (19283380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c440d986f0bb5cd0d2b54b000f66d219d485fe01156c83e521ca043343eaa`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5e005da41696b2a54a882c54042a6f1d0b17d46c35764e13dc483553b2972`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b06d561699b752f24ba95b01207841e01d0719dfbe6a672e99ab376e6935c`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa9ddd1a61f5cb64f47bed02502a9aa201f815f7771313483742408303a65b`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.7 MB (19715375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:85054315edda96f30ed9f7567edc068176f539f4823dd4dc9f573f205c60cfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27.2.0-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:f79c41f6313d87137a86a10b6766aa1a8d7fd7222566fc535e8b035ba5275d30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303408245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadc037faf2c53d92a835b8acd557af08233054e3c014a15ee63fcd6bd6b372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 20:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:04 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:58:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:58:06 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:58:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:58:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:58:56 GMT
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
	-	`sha256:bea7b5749b0c9fb1ac4216c0ec3cc34e8c4be1bce91440d5e1af1649c9c44b28`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d3dbb1662bf2bd051db933d8f25a808f934a2193a77362aabad59b3ea4662`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 517.4 KB (517436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841d1c8c7a9173bff32240c17bdffdf38c681b5b4397203e950a003472b2905`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810d7ba2db013f2f7325865ca49bb77484db37c509e0be28424d521b6e2a2d7`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a162087fe10bf8028abdf75d0405a7ef811f88a987ab854203312c22eb9861`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 18.7 MB (18677122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56da2e9f3099c19aedac3881cfe6bfb105ef07c87df79d1b0f0bc45b58e650`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d7596bf7393641bb335dc26dfb31a26d85fc8df54fa9f954191d85af23e6a1`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd2f20acdd7b9e4ec1e66f6ad8e1339f99f84d83c63e45954a6fb65ff14dce`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16dde64c46ae532c4d1498a92b6e7b848d486b49c8f468ececc93c64f815bf`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.3 MB (19283380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c440d986f0bb5cd0d2b54b000f66d219d485fe01156c83e521ca043343eaa`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5e005da41696b2a54a882c54042a6f1d0b17d46c35764e13dc483553b2972`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b06d561699b752f24ba95b01207841e01d0719dfbe6a672e99ab376e6935c`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa9ddd1a61f5cb64f47bed02502a9aa201f815f7771313483742408303a65b`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.7 MB (19715375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:5eebe2261795454a6c9a54eed64f81f6ebd7b007ec70efd6bf3fffd090ec4843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27.2.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:0609f36687bf0504b97ad2081e11e72b32ddeeaa13cec6b048e3203430ef3089
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199734114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e1d842fb99c5efb58e541674f93c74cd42646f4b55c3b595d31040d55bc8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 20:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:55:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:55:45 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:55:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:55:56 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:55:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:55:58 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:56:09 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:56:17 GMT
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
	-	`sha256:4cf2d920f1909f2588f1ff04da758a04650a2c83aa8846cdd27b355d5a3a977f`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d5e4634044af44742fd5ffcf53035c01b840441d1a6cbef4ac7c746079486`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 360.5 KB (360496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d90ca9a81e4b14450116f867b3fb9c986db7e6175327f0b8504e381923861`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e248f39ea321d362cd75a8d419e0ea56ae669b863c01760c1c8e4b3dddb81`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963453be438ca99012a6b206cb013b6e169d667b571731db178d8bb33f606b96`  
		Last Modified: Wed, 28 Aug 2024 20:56:27 GMT  
		Size: 18.6 MB (18648166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d3ae2221337464147d8ca5bf07cba7df651cea8324b58d3627e3dcfeb949c`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf2a088e2ea59c0a94284511a62711915af818e15bd695a7a25fd6624e26d2`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088754d192ca79a523ab3c6fdb3cecf0d5400910e48a70be1bc99b09c4d545`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ae88bbccf2cdc37064a22b1efaeec5ce004676d3da7f6fe9568b4421daa89`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.3 MB (19256026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30b29b13ead92894d4f6fb2e79593d75d134dfdd002ef8b65a4e79c03408b3c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039c01e50286e2d55794b477a1c9be4a1865ddc62c5d442e8d1ce8bf23ba99c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57d9a6f993df099347c867bae5736a2f45b5c6a82fac6d770c981623610e6c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08adb1197ed079a2603242de73317d9b6741e36aef8c5ca31089a2af9891fbf0`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.7 MB (19692868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:b0d5aafe0208821bdbe683e141cac9dac1a4ff30e5f56c7ae1359cbbeeb1d43f
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
$ docker pull docker@sha256:6ecc4797d7fd165cb322ff2249817633dc1f0063493eaaae51b060e96f817639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67051181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d1a0a6eeffb46012358ee49be7207e1ad437196afc818a45d84a616e40f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:949833a7d3a6cf9830ea4dbcc450cfacbb0f968be68136ddb32d8185ca036318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765f2662d20b39ba3767e01a47666f092782b3704d1a0304fc1fbdebd08c57e5`

```dockerfile
```

-	Layers:
	-	`sha256:dd1eb0c2b9a1555ad2485fbaa1ee07512f694cfcb2df8dbc423a401a28d390d1`  
		Last Modified: Fri, 06 Sep 2024 23:15:17 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:c358f3000b736a52dc1f5a6b5d38518d2d6dda817387096b925e61a0afce790a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62652673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04cb20b033eab2a1983d82c604ef6f9df0cc6e46b3e173df99cb5d1dd93fbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1926340345cfb0a7fe0ca0148b3e2e777781fefd99d6e747a3ecabf09ae3b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2a015819fd49c55db699b1a53efbbff73791fda9af7b14673ae3beb27fb50`

```dockerfile
```

-	Layers:
	-	`sha256:b4c1e47ed34c8d63a0aa353603824dc724b91b653deb4e926480c68c2718cfc9`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:90c3c35405f87d1995cd49f58f83aee5abec2d1c77dfdb71d171a8f6607e6d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61686124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727dcb0bc39c215426cb5ef8788e2988bafc6e6262dbb79674937465503c3333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a088502335df7562d09f9b2946827c1d66e655c0f05a52366dc651cd2f034711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f812bd756a4d09a43a8e9b5c02e8d6da59f1ba47a7f934adce0b71b2b8b6226`

```dockerfile
```

-	Layers:
	-	`sha256:c5b452f46f632ee1ce872f6357d8beea2ca96d34059d4cdc1144cd8daaad654f`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 38.1 KB (38071 bytes)  
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
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
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
$ docker pull docker@sha256:d387e5f5f938c28b52664293ba33f3c4b66a2ff4b7f0b74c5d05bdd94cafefba
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
$ docker pull docker@sha256:e3fbe21c151e4271d73fa228238bc61f32f660c550aa54e3527a460c27bac3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146696891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9187071f9b3d29959b0bf9a17b644db2d13e09317b504659a69884c6717ac1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7ebf14e366b1f6bb3a236c7afda2fa7f972ec82687bdfb1faa44ff909b3c7`  
		Last Modified: Wed, 28 Aug 2024 20:55:20 GMT  
		Size: 8.0 MB (7981883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70774fd8129e715db6bdde0a5fa9a8126035d57497c7abbf3918ff783e3839b9`  
		Last Modified: Wed, 28 Aug 2024 20:55:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75bde5fae086c68bd31219b257fd17de34da8ae7534ba873f2893aecb170265`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 17.3 MB (17266013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d280a0d728e728847e4bf2aea17b91f3d0b0341f060af4931e99f3701dd251a3`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e7e06e5fa6595fc74a6b371d01d11c33d00755afee8c9e5526b26db04bdca`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee3d5382660f041e5d6a4e7e5eed70a981eb51d8f65e980dc17b77257f5d1d`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e7d5e3ae6089103a06ae9421106617e42616bccfb18af4a99a047a339b59cf`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6843b239ba63d521157d7d1a46d9346bf6fd58eec87be84f52f99b62a8fb2d47`  
		Last Modified: Wed, 28 Aug 2024 20:55:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c047d9d5cf44cdaa49f139b96bfad8456b4544e7f8dac65b22512b54b5c27785`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 7.0 MB (7034976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8566c5e148875679770fa70b5d8461643fe4f3e523cc4c23fd5048921979993`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 98.7 KB (98665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e81cd465f9ee02216b68ffcd601579cf2b466ec9cfe9eab7d1848715d5efb6`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfc280f1208cfd219d0f5c9ce8a5485366216b0690ca15eac47242a174ec3ec`  
		Last Modified: Wed, 28 Aug 2024 21:48:47 GMT  
		Size: 52.4 MB (52400296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f850c0ae6138cdad5371b2e2f80f46619b8f1e83fd23719f35d80c4e68fd4`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494ac230758233bbef46064dc8f7048fff0763039a7c97d01acd30d1e1a6b16`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61d4b5e595f4a9dcd2d5b73dd64893b48b8b5c325e6c2a77f7d87c3bf774b63`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.0 MB (1023147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970a08325e433d212e5137f22b0c5f9ea602fe6d34c30ff0af92e85d826d457`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f824c9ac49392520b799e62abf06ca24190d5c747d6a8665d62f17c60adaf174`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468a19c79fccedbe38a88979c4a5da92b1a73c727a9b3fc58e11bbabd3e9256`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 22.8 MB (22835883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49084cd44b920e2654ce7a8f2bace247f0acd7ddfc481e9365b9c39c01dfe57`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b7cefe17c5a87b42bf6cfcec3b08ade5272c29f153f8fbcb770707bc1c20ccb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6630734a56a43074699439ce4c6d79ac0ec2972110823e0d46a936ece911b64f`

```dockerfile
```

-	Layers:
	-	`sha256:c50ad41cecb6f30ac11d08ace289d54c454da27e48229ef60c118eee48306b88`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:d1d6d5265119696d8fa9b883f813953c560c5d87ea128a57681239b576f62997
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
$ docker pull docker@sha256:dedb8ca94ea4fb6ebe843474b2bd4a83fcc62e0e0eb627f26c01b4c59f1b2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130583940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47c0fa2c99dc639ba53d1f4672320311666aef94ef754a85154cb34643e160`
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e2324570b800d68431bcd1527a19240c18f24a4a2db09d4af64123416a0dac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6904d9c6aeb45e8bc675ecc8e86a9245f6cc25f93106fdb8a573018a9fd6897`

```dockerfile
```

-	Layers:
	-	`sha256:cc266c857475eac80ae603ee53fb07ad4d431010ae69323caaa98350cbe467cf`  
		Last Modified: Sat, 07 Sep 2024 00:08:08 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:6c64cf2bc45a657f4d2e0a2f0ff2b5936162d7e515cf1f1b1f17be212214b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122794127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c9617e51d88ddbc6c962abf665b2684d162e98f1e7db7c90d3c3e26e60e0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 23:04:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:768e07a78d0469b61a393144d64bc89f2ccb4c064a0840fa084608fd9df23681`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 16.6 MB (16578255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafc33deb96055e74113c481a46eedd6848e4c37f47a947e95bc00873676216b`  
		Last Modified: Sat, 07 Sep 2024 02:16:27 GMT  
		Size: 17.1 MB (17114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078bab93e6056ebedd87d04608013d117aa2d71c995f448ffa5a60593084e663`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 17.8 MB (17783304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a1f160ead860eaeddae9242ae47d1dd8f7abdb66d8677a4f14f0a5dec36ec6`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8815fd989763fcf09cd8bfe9b1d4039d1ae6531133986da007b4ed92cfcddfa5`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7820cfcff68a26fa4723d5c775e3cd2f10cf7be92851b9e40b04d79fd848e`  
		Last Modified: Sat, 07 Sep 2024 02:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b605a03c2af2648b284df44c2d8bc710b28f23338a3ebb70f5a3047cad00c4`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 7.0 MB (6984324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405a8df98622f569cf7b88ef15211e61e4c543082eaa2b30a3e76e2e2ac95a7`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 88.4 KB (88406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f79cde32ec2b8dc0a6871de3430e572d4716a42da52409816e851ecd10862`  
		Last Modified: Sat, 07 Sep 2024 12:57:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f05c610fc9626914870671fd9d807d9a314fbc86fc92329649b296aa8eecc5`  
		Last Modified: Sat, 07 Sep 2024 12:57:24 GMT  
		Size: 53.1 MB (53062920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20753b82dac7a8924118b4c44f95f2a353c846980a543264962398fe1ede0a5b`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63167fc90a13832813b8ec1c0e9db7400a1baf763cfd6ab7ddcd71b833c952af`  
		Last Modified: Sat, 07 Sep 2024 12:57:23 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:14cea9226311058793710312daf3d8395bc62f50a1f9861629f24ecb2cab9fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba06ff4b58fc091ffe40153f849c5333f161856fcfe9ec5ceec02adfc8939ff`

```dockerfile
```

-	Layers:
	-	`sha256:09ed20c1be42eafbdfa006779df99c7a8be62c9dfae3e72964643fee7856d593`  
		Last Modified: Sat, 07 Sep 2024 12:57:21 GMT  
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
$ docker pull docker@sha256:07546d30ede0a05226bf16bd88fc0a63c9facc86586728958b4c80192695068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:0609f36687bf0504b97ad2081e11e72b32ddeeaa13cec6b048e3203430ef3089
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199734114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e1d842fb99c5efb58e541674f93c74cd42646f4b55c3b595d31040d55bc8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 20:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:55:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:55:45 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:55:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:55:56 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:55:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:55:58 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:56:09 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:56:17 GMT
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
	-	`sha256:4cf2d920f1909f2588f1ff04da758a04650a2c83aa8846cdd27b355d5a3a977f`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d5e4634044af44742fd5ffcf53035c01b840441d1a6cbef4ac7c746079486`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 360.5 KB (360496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d90ca9a81e4b14450116f867b3fb9c986db7e6175327f0b8504e381923861`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e248f39ea321d362cd75a8d419e0ea56ae669b863c01760c1c8e4b3dddb81`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963453be438ca99012a6b206cb013b6e169d667b571731db178d8bb33f606b96`  
		Last Modified: Wed, 28 Aug 2024 20:56:27 GMT  
		Size: 18.6 MB (18648166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d3ae2221337464147d8ca5bf07cba7df651cea8324b58d3627e3dcfeb949c`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf2a088e2ea59c0a94284511a62711915af818e15bd695a7a25fd6624e26d2`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088754d192ca79a523ab3c6fdb3cecf0d5400910e48a70be1bc99b09c4d545`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ae88bbccf2cdc37064a22b1efaeec5ce004676d3da7f6fe9568b4421daa89`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.3 MB (19256026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30b29b13ead92894d4f6fb2e79593d75d134dfdd002ef8b65a4e79c03408b3c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039c01e50286e2d55794b477a1c9be4a1865ddc62c5d442e8d1ce8bf23ba99c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57d9a6f993df099347c867bae5736a2f45b5c6a82fac6d770c981623610e6c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08adb1197ed079a2603242de73317d9b6741e36aef8c5ca31089a2af9891fbf0`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.7 MB (19692868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:f79c41f6313d87137a86a10b6766aa1a8d7fd7222566fc535e8b035ba5275d30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303408245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadc037faf2c53d92a835b8acd557af08233054e3c014a15ee63fcd6bd6b372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 20:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:04 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:58:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:58:06 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:58:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:58:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:58:56 GMT
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
	-	`sha256:bea7b5749b0c9fb1ac4216c0ec3cc34e8c4be1bce91440d5e1af1649c9c44b28`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d3dbb1662bf2bd051db933d8f25a808f934a2193a77362aabad59b3ea4662`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 517.4 KB (517436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841d1c8c7a9173bff32240c17bdffdf38c681b5b4397203e950a003472b2905`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810d7ba2db013f2f7325865ca49bb77484db37c509e0be28424d521b6e2a2d7`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a162087fe10bf8028abdf75d0405a7ef811f88a987ab854203312c22eb9861`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 18.7 MB (18677122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56da2e9f3099c19aedac3881cfe6bfb105ef07c87df79d1b0f0bc45b58e650`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d7596bf7393641bb335dc26dfb31a26d85fc8df54fa9f954191d85af23e6a1`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd2f20acdd7b9e4ec1e66f6ad8e1339f99f84d83c63e45954a6fb65ff14dce`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16dde64c46ae532c4d1498a92b6e7b848d486b49c8f468ececc93c64f815bf`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.3 MB (19283380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c440d986f0bb5cd0d2b54b000f66d219d485fe01156c83e521ca043343eaa`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5e005da41696b2a54a882c54042a6f1d0b17d46c35764e13dc483553b2972`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b06d561699b752f24ba95b01207841e01d0719dfbe6a672e99ab376e6935c`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa9ddd1a61f5cb64f47bed02502a9aa201f815f7771313483742408303a65b`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.7 MB (19715375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:85054315edda96f30ed9f7567edc068176f539f4823dd4dc9f573f205c60cfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:f79c41f6313d87137a86a10b6766aa1a8d7fd7222566fc535e8b035ba5275d30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303408245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadc037faf2c53d92a835b8acd557af08233054e3c014a15ee63fcd6bd6b372`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 20:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:57:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:04 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:58:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:58:06 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:58:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:58:33 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:58:56 GMT
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
	-	`sha256:bea7b5749b0c9fb1ac4216c0ec3cc34e8c4be1bce91440d5e1af1649c9c44b28`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d3dbb1662bf2bd051db933d8f25a808f934a2193a77362aabad59b3ea4662`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 517.4 KB (517436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c841d1c8c7a9173bff32240c17bdffdf38c681b5b4397203e950a003472b2905`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810d7ba2db013f2f7325865ca49bb77484db37c509e0be28424d521b6e2a2d7`  
		Last Modified: Wed, 28 Aug 2024 20:59:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a162087fe10bf8028abdf75d0405a7ef811f88a987ab854203312c22eb9861`  
		Last Modified: Wed, 28 Aug 2024 20:59:02 GMT  
		Size: 18.7 MB (18677122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56da2e9f3099c19aedac3881cfe6bfb105ef07c87df79d1b0f0bc45b58e650`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d7596bf7393641bb335dc26dfb31a26d85fc8df54fa9f954191d85af23e6a1`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd2f20acdd7b9e4ec1e66f6ad8e1339f99f84d83c63e45954a6fb65ff14dce`  
		Last Modified: Wed, 28 Aug 2024 20:58:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16dde64c46ae532c4d1498a92b6e7b848d486b49c8f468ececc93c64f815bf`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.3 MB (19283380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c440d986f0bb5cd0d2b54b000f66d219d485fe01156c83e521ca043343eaa`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a5e005da41696b2a54a882c54042a6f1d0b17d46c35764e13dc483553b2972`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b06d561699b752f24ba95b01207841e01d0719dfbe6a672e99ab376e6935c`  
		Last Modified: Wed, 28 Aug 2024 20:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa9ddd1a61f5cb64f47bed02502a9aa201f815f7771313483742408303a65b`  
		Last Modified: Wed, 28 Aug 2024 20:59:01 GMT  
		Size: 19.7 MB (19715375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:5eebe2261795454a6c9a54eed64f81f6ebd7b007ec70efd6bf3fffd090ec4843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:0609f36687bf0504b97ad2081e11e72b32ddeeaa13cec6b048e3203430ef3089
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199734114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e1d842fb99c5efb58e541674f93c74cd42646f4b55c3b595d31040d55bc8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 20:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 20:55:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 28 Aug 2024 20:55:45 GMT
ENV DOCKER_VERSION=27.2.0
# Wed, 28 Aug 2024 20:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.0.zip
# Wed, 28 Aug 2024 20:55:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:55:56 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Wed, 28 Aug 2024 20:55:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Wed, 28 Aug 2024 20:55:58 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Wed, 28 Aug 2024 20:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 28 Aug 2024 20:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 28 Aug 2024 20:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 28 Aug 2024 20:56:09 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 28 Aug 2024 20:56:17 GMT
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
	-	`sha256:4cf2d920f1909f2588f1ff04da758a04650a2c83aa8846cdd27b355d5a3a977f`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d5e4634044af44742fd5ffcf53035c01b840441d1a6cbef4ac7c746079486`  
		Last Modified: Wed, 28 Aug 2024 20:56:26 GMT  
		Size: 360.5 KB (360496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d90ca9a81e4b14450116f867b3fb9c986db7e6175327f0b8504e381923861`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e248f39ea321d362cd75a8d419e0ea56ae669b863c01760c1c8e4b3dddb81`  
		Last Modified: Wed, 28 Aug 2024 20:56:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963453be438ca99012a6b206cb013b6e169d667b571731db178d8bb33f606b96`  
		Last Modified: Wed, 28 Aug 2024 20:56:27 GMT  
		Size: 18.6 MB (18648166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d3ae2221337464147d8ca5bf07cba7df651cea8324b58d3627e3dcfeb949c`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf2a088e2ea59c0a94284511a62711915af818e15bd695a7a25fd6624e26d2`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71088754d192ca79a523ab3c6fdb3cecf0d5400910e48a70be1bc99b09c4d545`  
		Last Modified: Wed, 28 Aug 2024 20:56:23 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ae88bbccf2cdc37064a22b1efaeec5ce004676d3da7f6fe9568b4421daa89`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.3 MB (19256026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30b29b13ead92894d4f6fb2e79593d75d134dfdd002ef8b65a4e79c03408b3c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039c01e50286e2d55794b477a1c9be4a1865ddc62c5d442e8d1ce8bf23ba99c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57d9a6f993df099347c867bae5736a2f45b5c6a82fac6d770c981623610e6c`  
		Last Modified: Wed, 28 Aug 2024 20:56:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08adb1197ed079a2603242de73317d9b6741e36aef8c5ca31089a2af9891fbf0`  
		Last Modified: Wed, 28 Aug 2024 20:56:24 GMT  
		Size: 19.7 MB (19692868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
