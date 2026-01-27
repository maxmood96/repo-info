<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.2`](#docker292)
-	[`docker:29.2-cli`](#docker292-cli)
-	[`docker:29.2-dind`](#docker292-dind)
-	[`docker:29.2-dind-rootless`](#docker292-dind-rootless)
-	[`docker:29.2-windowsservercore`](#docker292-windowsservercore)
-	[`docker:29.2-windowsservercore-ltsc2022`](#docker292-windowsservercore-ltsc2022)
-	[`docker:29.2-windowsservercore-ltsc2025`](#docker292-windowsservercore-ltsc2025)
-	[`docker:29.2.0`](#docker2920)
-	[`docker:29.2.0-alpine3.23`](#docker2920-alpine323)
-	[`docker:29.2.0-cli`](#docker2920-cli)
-	[`docker:29.2.0-cli-alpine3.23`](#docker2920-cli-alpine323)
-	[`docker:29.2.0-dind`](#docker2920-dind)
-	[`docker:29.2.0-dind-alpine3.23`](#docker2920-dind-alpine323)
-	[`docker:29.2.0-dind-rootless`](#docker2920-dind-rootless)
-	[`docker:29.2.0-windowsservercore`](#docker2920-windowsservercore)
-	[`docker:29.2.0-windowsservercore-ltsc2022`](#docker2920-windowsservercore-ltsc2022)
-	[`docker:29.2.0-windowsservercore-ltsc2025`](#docker2920-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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

### `docker:29` - linux; amd64

```console
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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

### `docker:29-dind` - linux; amd64

```console
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:438cc9fb790caae654a29f2abdbe48bc2713f4bacc2bd412b7d2c60e458dd7e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d996fddf7545f36bb88186f0f93d91be8a344f66e1bf533963ef43af9f55ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164593926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13178a6a1a242b18e6c4d5026ea85091f37708edeb65a4c272ae38f5c5625ffc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
# Tue, 27 Jan 2026 00:10:27 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:10:28 GMT
USER rootless
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fe2f1fa32645d48d001a89d38a430aadf23b75f1d0e5ac13f1b01167cb9832`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 3.4 MB (3419926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa627d12989120878617b0ff6a40178ee7aa2784f5f2458842b19940aa939d`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a31c2a645fd1fcc13c6428f0ac8ac05191dbdc4e0f1b4534d0d55200cbd33f`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aadcb781d1119f67cfaa92f5bde31a037fe5d04e96a4c69e91c34cfab5cb01`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 17.4 MB (17375881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a4911b0841bb43582f002f95adfb02250cfbb041acf646784c23c49170dc0`  
		Last Modified: Tue, 27 Jan 2026 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eecdfcfd5d851df2dcb6b062c1bcae9d817e4341b90becdf8d55e6507a44f25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c62ce9d4e97e2653e88e62ec6e16475ab34150bd8b5bc28726aa2540e7836a`

```dockerfile
```

-	Layers:
	-	`sha256:c25d5569116a154c4af8fb0680af4fc57f9c5115376f49cd584c859895dd7b2b`  
		Last Modified: Tue, 27 Jan 2026 00:10:33 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1e508668ee940f39e31e6a4628b6f9a0e413322a092f5331f669f2b3e20d5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154353821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a552b8a628d1f17e4a8efdedba1acc4ba1ceccd944139be93f60b8792dca72`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
# Tue, 27 Jan 2026 00:09:56 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:09:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdb84c2218b48c5b9766cb97850e54d443b737e5e4530a3f38c489d7e8f4089`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 3.4 MB (3394372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d57bda1cb43b60c1cc6a6fb3714df5f8210c32786cc45199eeee8cbdc14de`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e18bfd676e1a7766203504fd22927105c9de3a71a993ba1db8736ea1edeb25`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b129068910c279c84e85bc7ac66a57ed83092823bb7f7c6472e14dd0b3e2a5e8`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 17.7 MB (17710524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706f08ecf2c655ec8c075aee1b4e8927526ca15e209be5619b920a56c0f2b74a`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ee2d83c7bb434663d31bce1757b12c86071167fc765d1b6c6d7ee002f8eb0be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f5d2f47b1b608f50f1efb950866fd3f2f97cf8b013382b80ce6952b1cd4171`

```dockerfile
```

-	Layers:
	-	`sha256:48499ecd27366c720d757644ac58e98c7a3843f0e5128ab6ea6487df0f704a8d`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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

### `docker:29.2` - linux; amd64

```console
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-cli`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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

### `docker:29.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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

### `docker:29.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind-rootless`

```console
$ docker pull docker@sha256:438cc9fb790caae654a29f2abdbe48bc2713f4bacc2bd412b7d2c60e458dd7e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d996fddf7545f36bb88186f0f93d91be8a344f66e1bf533963ef43af9f55ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164593926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13178a6a1a242b18e6c4d5026ea85091f37708edeb65a4c272ae38f5c5625ffc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
# Tue, 27 Jan 2026 00:10:27 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:10:28 GMT
USER rootless
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fe2f1fa32645d48d001a89d38a430aadf23b75f1d0e5ac13f1b01167cb9832`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 3.4 MB (3419926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa627d12989120878617b0ff6a40178ee7aa2784f5f2458842b19940aa939d`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a31c2a645fd1fcc13c6428f0ac8ac05191dbdc4e0f1b4534d0d55200cbd33f`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aadcb781d1119f67cfaa92f5bde31a037fe5d04e96a4c69e91c34cfab5cb01`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 17.4 MB (17375881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a4911b0841bb43582f002f95adfb02250cfbb041acf646784c23c49170dc0`  
		Last Modified: Tue, 27 Jan 2026 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eecdfcfd5d851df2dcb6b062c1bcae9d817e4341b90becdf8d55e6507a44f25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c62ce9d4e97e2653e88e62ec6e16475ab34150bd8b5bc28726aa2540e7836a`

```dockerfile
```

-	Layers:
	-	`sha256:c25d5569116a154c4af8fb0680af4fc57f9c5115376f49cd584c859895dd7b2b`  
		Last Modified: Tue, 27 Jan 2026 00:10:33 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1e508668ee940f39e31e6a4628b6f9a0e413322a092f5331f669f2b3e20d5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154353821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a552b8a628d1f17e4a8efdedba1acc4ba1ceccd944139be93f60b8792dca72`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
# Tue, 27 Jan 2026 00:09:56 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:09:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdb84c2218b48c5b9766cb97850e54d443b737e5e4530a3f38c489d7e8f4089`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 3.4 MB (3394372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d57bda1cb43b60c1cc6a6fb3714df5f8210c32786cc45199eeee8cbdc14de`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e18bfd676e1a7766203504fd22927105c9de3a71a993ba1db8736ea1edeb25`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b129068910c279c84e85bc7ac66a57ed83092823bb7f7c6472e14dd0b3e2a5e8`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 17.7 MB (17710524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706f08ecf2c655ec8c075aee1b4e8927526ca15e209be5619b920a56c0f2b74a`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ee2d83c7bb434663d31bce1757b12c86071167fc765d1b6c6d7ee002f8eb0be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f5d2f47b1b608f50f1efb950866fd3f2f97cf8b013382b80ce6952b1cd4171`

```dockerfile
```

-	Layers:
	-	`sha256:48499ecd27366c720d757644ac58e98c7a3843f0e5128ab6ea6487df0f704a8d`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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

### `docker:29.2.0` - linux; amd64

```console
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-alpine3.23`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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

### `docker:29.2.0-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-cli`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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

### `docker:29.2.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-cli-alpine3.23`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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

### `docker:29.2.0-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-dind`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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

### `docker:29.2.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-dind-alpine3.23`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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

### `docker:29.2.0-dind-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-dind-rootless`

```console
$ docker pull docker@sha256:438cc9fb790caae654a29f2abdbe48bc2713f4bacc2bd412b7d2c60e458dd7e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d996fddf7545f36bb88186f0f93d91be8a344f66e1bf533963ef43af9f55ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164593926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13178a6a1a242b18e6c4d5026ea85091f37708edeb65a4c272ae38f5c5625ffc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
# Tue, 27 Jan 2026 00:10:27 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:10:28 GMT
USER rootless
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fe2f1fa32645d48d001a89d38a430aadf23b75f1d0e5ac13f1b01167cb9832`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 3.4 MB (3419926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa627d12989120878617b0ff6a40178ee7aa2784f5f2458842b19940aa939d`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a31c2a645fd1fcc13c6428f0ac8ac05191dbdc4e0f1b4534d0d55200cbd33f`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aadcb781d1119f67cfaa92f5bde31a037fe5d04e96a4c69e91c34cfab5cb01`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 17.4 MB (17375881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a4911b0841bb43582f002f95adfb02250cfbb041acf646784c23c49170dc0`  
		Last Modified: Tue, 27 Jan 2026 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eecdfcfd5d851df2dcb6b062c1bcae9d817e4341b90becdf8d55e6507a44f25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c62ce9d4e97e2653e88e62ec6e16475ab34150bd8b5bc28726aa2540e7836a`

```dockerfile
```

-	Layers:
	-	`sha256:c25d5569116a154c4af8fb0680af4fc57f9c5115376f49cd584c859895dd7b2b`  
		Last Modified: Tue, 27 Jan 2026 00:10:33 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1e508668ee940f39e31e6a4628b6f9a0e413322a092f5331f669f2b3e20d5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154353821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a552b8a628d1f17e4a8efdedba1acc4ba1ceccd944139be93f60b8792dca72`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
# Tue, 27 Jan 2026 00:09:56 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:09:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdb84c2218b48c5b9766cb97850e54d443b737e5e4530a3f38c489d7e8f4089`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 3.4 MB (3394372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d57bda1cb43b60c1cc6a6fb3714df5f8210c32786cc45199eeee8cbdc14de`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e18bfd676e1a7766203504fd22927105c9de3a71a993ba1db8736ea1edeb25`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b129068910c279c84e85bc7ac66a57ed83092823bb7f7c6472e14dd0b3e2a5e8`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 17.7 MB (17710524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706f08ecf2c655ec8c075aee1b4e8927526ca15e209be5619b920a56c0f2b74a`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ee2d83c7bb434663d31bce1757b12c86071167fc765d1b6c6d7ee002f8eb0be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f5d2f47b1b608f50f1efb950866fd3f2f97cf8b013382b80ce6952b1cd4171`

```dockerfile
```

-	Layers:
	-	`sha256:48499ecd27366c720d757644ac58e98c7a3843f0e5128ab6ea6487df0f704a8d`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.0-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2.0-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2.0-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:438cc9fb790caae654a29f2abdbe48bc2713f4bacc2bd412b7d2c60e458dd7e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d996fddf7545f36bb88186f0f93d91be8a344f66e1bf533963ef43af9f55ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164593926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13178a6a1a242b18e6c4d5026ea85091f37708edeb65a4c272ae38f5c5625ffc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
# Tue, 27 Jan 2026 00:10:27 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:10:28 GMT
USER rootless
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fe2f1fa32645d48d001a89d38a430aadf23b75f1d0e5ac13f1b01167cb9832`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 3.4 MB (3419926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa627d12989120878617b0ff6a40178ee7aa2784f5f2458842b19940aa939d`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a31c2a645fd1fcc13c6428f0ac8ac05191dbdc4e0f1b4534d0d55200cbd33f`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aadcb781d1119f67cfaa92f5bde31a037fe5d04e96a4c69e91c34cfab5cb01`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 17.4 MB (17375881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a4911b0841bb43582f002f95adfb02250cfbb041acf646784c23c49170dc0`  
		Last Modified: Tue, 27 Jan 2026 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eecdfcfd5d851df2dcb6b062c1bcae9d817e4341b90becdf8d55e6507a44f25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c62ce9d4e97e2653e88e62ec6e16475ab34150bd8b5bc28726aa2540e7836a`

```dockerfile
```

-	Layers:
	-	`sha256:c25d5569116a154c4af8fb0680af4fc57f9c5115376f49cd584c859895dd7b2b`  
		Last Modified: Tue, 27 Jan 2026 00:10:33 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1e508668ee940f39e31e6a4628b6f9a0e413322a092f5331f669f2b3e20d5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154353821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a552b8a628d1f17e4a8efdedba1acc4ba1ceccd944139be93f60b8792dca72`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
# Tue, 27 Jan 2026 00:09:56 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:09:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdb84c2218b48c5b9766cb97850e54d443b737e5e4530a3f38c489d7e8f4089`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 3.4 MB (3394372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d57bda1cb43b60c1cc6a6fb3714df5f8210c32786cc45199eeee8cbdc14de`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e18bfd676e1a7766203504fd22927105c9de3a71a993ba1db8736ea1edeb25`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b129068910c279c84e85bc7ac66a57ed83092823bb7f7c6472e14dd0b3e2a5e8`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 17.7 MB (17710524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706f08ecf2c655ec8c075aee1b4e8927526ca15e209be5619b920a56c0f2b74a`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ee2d83c7bb434663d31bce1757b12c86071167fc765d1b6c6d7ee002f8eb0be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f5d2f47b1b608f50f1efb950866fd3f2f97cf8b013382b80ce6952b1cd4171`

```dockerfile
```

-	Layers:
	-	`sha256:48499ecd27366c720d757644ac58e98c7a3843f0e5128ab6ea6487df0f704a8d`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:6a58fe0da3d9c36bae9adb37ec6af8cb07b5a1d02aa72ae5ad370d7ecbafdfcd
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
$ docker pull docker@sha256:9bb49d773225fa1399ac5b4e94ecacc0e2cc1ef212d9904f718d8dd64d44a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143796777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2853506810b6d23bcc6cc15edadf7194eed9c50bb399012471adae3bce954d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:59b83af396dc6c198cdb543ff942a19ff7012e60ecc6eb88292bb11a305c47fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07926bf0e0f5f09ab492af1a4e29c59ec15096c92c46d9e3c3230aa764a7b940`

```dockerfile
```

-	Layers:
	-	`sha256:403c86e6215de3cdbf8f3cb148ca5ec4cdf85bc8fb496b1e85fb932772d1d6b7`  
		Last Modified: Mon, 26 Jan 2026 23:11:16 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:869b9b652999843118ab332c545f477b22d4574816e2a22259ddedbb5ffa6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135628875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c1f48427e0a2c43d51849de071571d1478af762ce53040d8d42438325823`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:16 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:16 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56fdc881ae4006d1966c3abe5aecf0338b9b7e4b931a4663b9a0a64ad03ab4`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 7.3 MB (7271452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890df9cba84d7e2fa00160a630da3f3046ce4b01a07b6fd62cc9b98834879865`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 91.8 KB (91774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262217583bbae1e9077044a1fa3d1220e93249220901f3d485c78e1d0ac254eb`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe2e8b33a1cd69fd6851f2a078f9e661a6746523c52e2203127a2aed9499e`  
		Last Modified: Mon, 26 Jan 2026 23:11:29 GMT  
		Size: 62.0 MB (62028090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a539a56c775ad10aebdb4bfba411756516d9774ff7f744431c4e25a4b7d5f42`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d4d966cac60abc606c79f295a0317a9b0161f8446d6fffe960022c3d6990`  
		Last Modified: Mon, 26 Jan 2026 23:11:28 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5b5a37235f2f12ef08816eca202796de995d13f549bb97a6a125d7e90cfc7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e435e540d7d5656aa59bba21c6bb0bc84f75c15eab4ae14ad418668ff92a1c`

```dockerfile
```

-	Layers:
	-	`sha256:e843f9ae55a6322bb4d9ddfa90434837d2a8aa4f7a8194fe0ea5e692f01ac1f9`  
		Last Modified: Mon, 26 Jan 2026 23:11:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:1379588612aac43a6386eada87ba4a5fec3540e2d84516282160f4a500d985a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133712971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45327f00522e75123e85513ffe4702559385698e66cd6ab7a1106e1ed3eeec`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:09:30 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab35d8ff1fde1b10ce47b7c4d7ea74a7c7b3355d604e1d4d35f1482d1779676`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 6.6 MB (6572788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb0cd15b65c120a633b58252f489487d4dcc30c1817503dfd40a3826c9bc9`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 88.1 KB (88133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8197a80bb3a4aa49b9ea1fff42087cc310091c98ab6e9e04c518aaf9344445cf`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2874ef371b1504ca987f82393fc805b7ff86333e21b8babfa50153baf8ebfc76`  
		Last Modified: Mon, 26 Jan 2026 23:09:42 GMT  
		Size: 61.9 MB (61856942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fd02b54e537e150649b4544b627861be939cf8abcf5fc35a37a6dbbf1b0b0`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f309f432ee07008ec05bff659ea84e9593906c0e99492f75e895e4a62797afd`  
		Last Modified: Mon, 26 Jan 2026 23:09:41 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e684d8fafd63aab580d668988fff70cb79948ecfa17794aded4e0f61024cea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c33553242db8e405c72f4e5c90551f14690521927d3c32467772487d4697`

```dockerfile
```

-	Layers:
	-	`sha256:f0248531574e8e2b46bf36dadc12965662dd0cc201cf8fa1ac2c9f4e7b2dcd9a`  
		Last Modified: Mon, 26 Jan 2026 23:09:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2256a5ca9fe82191c338f41cae426634cc47f22722dae678a35e78f3f6b2ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133247585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5aa387f6e7d3cdfb8fc5e572a44df926194b08c7a37062cff2ab28850e4e74`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:8e242fa525053b6be8f63b04894c9aff719a1f40a21c8ac0f63332423ab7f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0de2412a811bcdf046e2de706f57267517b2e9d126904a69872bb9eb6e088d0`

```dockerfile
```

-	Layers:
	-	`sha256:e26202726bdfdd7664fb7a739ad513e9b49f387e7b82d26167af0be198a84d98`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
